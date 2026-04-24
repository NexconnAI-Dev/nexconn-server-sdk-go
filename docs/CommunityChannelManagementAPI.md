# CommunityChannelManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddCommunityChannelUserGroupUsers**](CommunityChannelManagementAPI.md#AddCommunityChannelUserGroupUsers) | **Post** /v4/community-channel/user-group/user/add | Add community channel user group users
[**AddCommunityChannelUserGroups**](CommunityChannelManagementAPI.md#AddCommunityChannelUserGroups) | **Post** /v4/community-channel/user-group/add | Add community channel user groups
[**AddPrivateSubchannelMembers**](CommunityChannelManagementAPI.md#AddPrivateSubchannelMembers) | **Post** /v4/community-channel/private-subchannel/member/add | Add private subchannel members
[**BindCommunityChannelUserGroup**](CommunityChannelManagementAPI.md#BindCommunityChannelUserGroup) | **Post** /v4/community-channel/channel/user-group/bind | Bind community channel user group
[**CheckCommunityChannelMemberExist**](CommunityChannelManagementAPI.md#CheckCommunityChannelMemberExist) | **Post** /v4/community-channel/member/exist | Check community channel member exist
[**CreateCommunityChannel**](CommunityChannelManagementAPI.md#CreateCommunityChannel) | **Post** /v4/community-channel/create | Create community channel
[**CreateCommunitySubchannel**](CommunityChannelManagementAPI.md#CreateCommunitySubchannel) | **Post** /v4/community-channel/subchannel/create | Create community subchannel
[**DeleteCommunitySubchannel**](CommunityChannelManagementAPI.md#DeleteCommunitySubchannel) | **Post** /v4/community-channel/subchannel/delete | Delete community subchannel
[**DismissCommunityChannel**](CommunityChannelManagementAPI.md#DismissCommunityChannel) | **Post** /v4/community-channel/dismiss | Dismiss community channel
[**JoinCommunityChannel**](CommunityChannelManagementAPI.md#JoinCommunityChannel) | **Post** /v4/community-channel/join | Join community channel
[**ListCommunityChannelHistoryMessages**](CommunityChannelManagementAPI.md#ListCommunityChannelHistoryMessages) | **Post** /v4/community-channel/history-message/list | List community-channel history messages
[**ListCommunityChannelSubchannelUserGroups**](CommunityChannelManagementAPI.md#ListCommunityChannelSubchannelUserGroups) | **Post** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups
[**ListCommunityChannelUserGroupSubchannels**](CommunityChannelManagementAPI.md#ListCommunityChannelUserGroupSubchannels) | **Post** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels
[**ListCommunityChannelUserGroups**](CommunityChannelManagementAPI.md#ListCommunityChannelUserGroups) | **Post** /v4/community-channel/user-group/list | List community channel user groups
[**ListCommunityChannelUserUserGroups**](CommunityChannelManagementAPI.md#ListCommunityChannelUserUserGroups) | **Post** /v4/community-channel/user/user-group/list | List community channel user user groups
[**ListCommunitySubchannels**](CommunityChannelManagementAPI.md#ListCommunitySubchannels) | **Post** /v4/community-channel/subchannel/list | List community subchannels
[**ListCommunityUserSubchannels**](CommunityChannelManagementAPI.md#ListCommunityUserSubchannels) | **Post** /v4/community-channel/user/subchannel/list | List community user subchannels
[**ListPrivateSubchannelMembers**](CommunityChannelManagementAPI.md#ListPrivateSubchannelMembers) | **Post** /v4/community-channel/private-subchannel/member/list | List private subchannel members
[**QuitCommunityChannel**](CommunityChannelManagementAPI.md#QuitCommunityChannel) | **Post** /v4/community-channel/leave | Leave community channel
[**RemoveCommunityChannelUserGroupUsers**](CommunityChannelManagementAPI.md#RemoveCommunityChannelUserGroupUsers) | **Post** /v4/community-channel/user-group/user/remove | Remove community channel user group users
[**RemoveCommunityChannelUserGroups**](CommunityChannelManagementAPI.md#RemoveCommunityChannelUserGroups) | **Post** /v4/community-channel/user-group/remove | Delete community channel user groups
[**RemovePrivateSubchannelMembers**](CommunityChannelManagementAPI.md#RemovePrivateSubchannelMembers) | **Post** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members
[**UnbindCommunityChannelUserGroup**](CommunityChannelManagementAPI.md#UnbindCommunityChannelUserGroup) | **Post** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group
[**UpdateCommunityChannelInfo**](CommunityChannelManagementAPI.md#UpdateCommunityChannelInfo) | **Post** /v4/community-channel/update | Update community channel info
[**UpdateCommunitySubchannelType**](CommunityChannelManagementAPI.md#UpdateCommunitySubchannelType) | **Post** /v4/community-channel/subchannel-type/update | Update community subchannel type



## AddCommunityChannelUserGroupUsers

> CodeOnlyResponse AddCommunityChannelUserGroupUsers(ctx).CommunityChannelUserGroupUsersRequest(communityChannelUserGroupUsersRequest).Execute()

Add community channel user group users

### Example

```go
package main

import (
	"context"
	"fmt"
	"log"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupUsersRequest := *openapiclient.NewCommunityChannelUserGroupUsersRequest("ChannelId_example", "UserGroupId_example", []string{"UserIds_example"}) // CommunityChannelUserGroupUsersRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.AddCommunityChannelUserGroupUsers(context.Background()).CommunityChannelUserGroupUsersRequest(communityChannelUserGroupUsersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.AddCommunityChannelUserGroupUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddCommunityChannelUserGroupUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.AddCommunityChannelUserGroupUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddCommunityChannelUserGroupUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupUsersRequest** | [**CommunityChannelUserGroupUsersRequest**](CommunityChannelUserGroupUsersRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AddCommunityChannelUserGroups

> CodeOnlyResponse AddCommunityChannelUserGroups(ctx).CommunityChannelUserGroupAddRequest(communityChannelUserGroupAddRequest).Execute()

Add community channel user groups

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupAddRequest := *openapiclient.NewCommunityChannelUserGroupAddRequest("ChannelId_example", []openapiclient.CommunityChannelUserGroupItem{*openapiclient.NewCommunityChannelUserGroupItem("UserGroupId_example")}) // CommunityChannelUserGroupAddRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.AddCommunityChannelUserGroups(context.Background()).CommunityChannelUserGroupAddRequest(communityChannelUserGroupAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.AddCommunityChannelUserGroups``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddCommunityChannelUserGroups`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.AddCommunityChannelUserGroups`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddCommunityChannelUserGroupsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupAddRequest** | [**CommunityChannelUserGroupAddRequest**](CommunityChannelUserGroupAddRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AddPrivateSubchannelMembers

> CodeOnlyResponse AddPrivateSubchannelMembers(ctx).CommunityPrivateSubchannelMembersRequest(communityPrivateSubchannelMembersRequest).Execute()

Add private subchannel members

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityPrivateSubchannelMembersRequest := *openapiclient.NewCommunityPrivateSubchannelMembersRequest("ChannelId_example", "SubchannelId_example", []string{"UserIds_example"}) // CommunityPrivateSubchannelMembersRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.AddPrivateSubchannelMembers(context.Background()).CommunityPrivateSubchannelMembersRequest(communityPrivateSubchannelMembersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.AddPrivateSubchannelMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddPrivateSubchannelMembers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.AddPrivateSubchannelMembers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddPrivateSubchannelMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityPrivateSubchannelMembersRequest** | [**CommunityPrivateSubchannelMembersRequest**](CommunityPrivateSubchannelMembersRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BindCommunityChannelUserGroup

> CodeOnlyResponse BindCommunityChannelUserGroup(ctx).CommunityChannelUserGroupBindingRequest(communityChannelUserGroupBindingRequest).Execute()

Bind community channel user group

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupBindingRequest := *openapiclient.NewCommunityChannelUserGroupBindingRequest("ChannelId_example", "SubchannelId_example", []string{"UserGroupIds_example"}) // CommunityChannelUserGroupBindingRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.BindCommunityChannelUserGroup(context.Background()).CommunityChannelUserGroupBindingRequest(communityChannelUserGroupBindingRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.BindCommunityChannelUserGroup``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BindCommunityChannelUserGroup`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.BindCommunityChannelUserGroup`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBindCommunityChannelUserGroupRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupBindingRequest** | [**CommunityChannelUserGroupBindingRequest**](CommunityChannelUserGroupBindingRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CheckCommunityChannelMemberExist

> CommunityChannelMemberExistResponse CheckCommunityChannelMemberExist(ctx).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()

Check community channel member exist

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelMemberRequest := *openapiclient.NewCommunityChannelMemberRequest("UserId_example", "ChannelId_example") // CommunityChannelMemberRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.CheckCommunityChannelMemberExist(context.Background()).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.CheckCommunityChannelMemberExist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CheckCommunityChannelMemberExist`: CommunityChannelMemberExistResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.CheckCommunityChannelMemberExist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCheckCommunityChannelMemberExistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md) |  | 

### Return type

[**CommunityChannelMemberExistResponse**](CommunityChannelMemberExistResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateCommunityChannel

> CodeOnlyResponse CreateCommunityChannel(ctx).CommunityChannelCreateRequest(communityChannelCreateRequest).Execute()

Create community channel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelCreateRequest := *openapiclient.NewCommunityChannelCreateRequest("UserId_example", "ChannelId_example", "Name_example") // CommunityChannelCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.CreateCommunityChannel(context.Background()).CommunityChannelCreateRequest(communityChannelCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.CreateCommunityChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateCommunityChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.CreateCommunityChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateCommunityChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelCreateRequest** | [**CommunityChannelCreateRequest**](CommunityChannelCreateRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateCommunitySubchannel

> CodeOnlyResponse CreateCommunitySubchannel(ctx).CommunitySubchannelCreateRequest(communitySubchannelCreateRequest).Execute()

Create community subchannel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communitySubchannelCreateRequest := *openapiclient.NewCommunitySubchannelCreateRequest("ChannelId_example", "SubchannelId_example") // CommunitySubchannelCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.CreateCommunitySubchannel(context.Background()).CommunitySubchannelCreateRequest(communitySubchannelCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.CreateCommunitySubchannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateCommunitySubchannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.CreateCommunitySubchannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateCommunitySubchannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communitySubchannelCreateRequest** | [**CommunitySubchannelCreateRequest**](CommunitySubchannelCreateRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteCommunitySubchannel

> CodeOnlyResponse DeleteCommunitySubchannel(ctx).CommunitySubchannelKeyRequest(communitySubchannelKeyRequest).Execute()

Delete community subchannel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communitySubchannelKeyRequest := *openapiclient.NewCommunitySubchannelKeyRequest("ChannelId_example", "SubchannelId_example") // CommunitySubchannelKeyRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.DeleteCommunitySubchannel(context.Background()).CommunitySubchannelKeyRequest(communitySubchannelKeyRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.DeleteCommunitySubchannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteCommunitySubchannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.DeleteCommunitySubchannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteCommunitySubchannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communitySubchannelKeyRequest** | [**CommunitySubchannelKeyRequest**](CommunitySubchannelKeyRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DismissCommunityChannel

> CodeOnlyResponse DismissCommunityChannel(ctx).CommunityChannelDismissRequest(communityChannelDismissRequest).Execute()

Dismiss community channel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelDismissRequest := *openapiclient.NewCommunityChannelDismissRequest("ChannelId_example") // CommunityChannelDismissRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.DismissCommunityChannel(context.Background()).CommunityChannelDismissRequest(communityChannelDismissRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.DismissCommunityChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DismissCommunityChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.DismissCommunityChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDismissCommunityChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelDismissRequest** | [**CommunityChannelDismissRequest**](CommunityChannelDismissRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## JoinCommunityChannel

> CodeOnlyResponse JoinCommunityChannel(ctx).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()

Join community channel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelMemberRequest := *openapiclient.NewCommunityChannelMemberRequest("UserId_example", "ChannelId_example") // CommunityChannelMemberRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.JoinCommunityChannel(context.Background()).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.JoinCommunityChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `JoinCommunityChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.JoinCommunityChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiJoinCommunityChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelHistoryMessages

> MessageHistoryResponse ListCommunityChannelHistoryMessages(ctx).CommunityChannelHistoryMessageListRequest(communityChannelHistoryMessageListRequest).Execute()

List community-channel history messages

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelHistoryMessageListRequest := *openapiclient.NewCommunityChannelHistoryMessageListRequest("ChannelId_example", "SubchannelId_example", int64(123), int64(123)) // CommunityChannelHistoryMessageListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityChannelHistoryMessages(context.Background()).CommunityChannelHistoryMessageListRequest(communityChannelHistoryMessageListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityChannelHistoryMessages``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelHistoryMessages`: MessageHistoryResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityChannelHistoryMessages`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelHistoryMessagesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelHistoryMessageListRequest** | [**CommunityChannelHistoryMessageListRequest**](CommunityChannelHistoryMessageListRequest.md) |  | 

### Return type

[**MessageHistoryResponse**](MessageHistoryResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelSubchannelUserGroups

> CommunityChannelSubchannelUserGroupListResponse ListCommunityChannelSubchannelUserGroups(ctx).CommunityChannelSubchannelUserGroupListRequest(communityChannelSubchannelUserGroupListRequest).Execute()

List community channel subchannel user groups

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelSubchannelUserGroupListRequest := *openapiclient.NewCommunityChannelSubchannelUserGroupListRequest("ChannelId_example", "SubchannelId_example") // CommunityChannelSubchannelUserGroupListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityChannelSubchannelUserGroups(context.Background()).CommunityChannelSubchannelUserGroupListRequest(communityChannelSubchannelUserGroupListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityChannelSubchannelUserGroups``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelSubchannelUserGroups`: CommunityChannelSubchannelUserGroupListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityChannelSubchannelUserGroups`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelSubchannelUserGroupsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelSubchannelUserGroupListRequest** | [**CommunityChannelSubchannelUserGroupListRequest**](CommunityChannelSubchannelUserGroupListRequest.md) |  | 

### Return type

[**CommunityChannelSubchannelUserGroupListResponse**](CommunityChannelSubchannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelUserGroupSubchannels

> CommunityChannelUserGroupSubchannelListResponse ListCommunityChannelUserGroupSubchannels(ctx).CommunityChannelUserGroupSubchannelListRequest(communityChannelUserGroupSubchannelListRequest).Execute()

List community channel user group subchannels

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupSubchannelListRequest := *openapiclient.NewCommunityChannelUserGroupSubchannelListRequest("ChannelId_example", "UserGroupId_example") // CommunityChannelUserGroupSubchannelListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityChannelUserGroupSubchannels(context.Background()).CommunityChannelUserGroupSubchannelListRequest(communityChannelUserGroupSubchannelListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityChannelUserGroupSubchannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelUserGroupSubchannels`: CommunityChannelUserGroupSubchannelListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityChannelUserGroupSubchannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelUserGroupSubchannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupSubchannelListRequest** | [**CommunityChannelUserGroupSubchannelListRequest**](CommunityChannelUserGroupSubchannelListRequest.md) |  | 

### Return type

[**CommunityChannelUserGroupSubchannelListResponse**](CommunityChannelUserGroupSubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelUserGroups

> CommunityChannelUserGroupListResponse ListCommunityChannelUserGroups(ctx).CommunityChannelUserGroupListRequest(communityChannelUserGroupListRequest).Execute()

List community channel user groups

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupListRequest := *openapiclient.NewCommunityChannelUserGroupListRequest("ChannelId_example") // CommunityChannelUserGroupListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityChannelUserGroups(context.Background()).CommunityChannelUserGroupListRequest(communityChannelUserGroupListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityChannelUserGroups``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelUserGroups`: CommunityChannelUserGroupListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityChannelUserGroups`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelUserGroupsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupListRequest** | [**CommunityChannelUserGroupListRequest**](CommunityChannelUserGroupListRequest.md) |  | 

### Return type

[**CommunityChannelUserGroupListResponse**](CommunityChannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelUserUserGroups

> CommunityChannelUserUserGroupListResponse ListCommunityChannelUserUserGroups(ctx).CommunityChannelUserUserGroupListRequest(communityChannelUserUserGroupListRequest).Execute()

List community channel user user groups

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserUserGroupListRequest := *openapiclient.NewCommunityChannelUserUserGroupListRequest("ChannelId_example", "UserId_example") // CommunityChannelUserUserGroupListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityChannelUserUserGroups(context.Background()).CommunityChannelUserUserGroupListRequest(communityChannelUserUserGroupListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityChannelUserUserGroups``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelUserUserGroups`: CommunityChannelUserUserGroupListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityChannelUserUserGroups`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelUserUserGroupsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserUserGroupListRequest** | [**CommunityChannelUserUserGroupListRequest**](CommunityChannelUserUserGroupListRequest.md) |  | 

### Return type

[**CommunityChannelUserUserGroupListResponse**](CommunityChannelUserUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunitySubchannels

> CommunitySubchannelListResponse ListCommunitySubchannels(ctx).CommunitySubchannelListRequest(communitySubchannelListRequest).Execute()

List community subchannels

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communitySubchannelListRequest := *openapiclient.NewCommunitySubchannelListRequest("ChannelId_example") // CommunitySubchannelListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunitySubchannels(context.Background()).CommunitySubchannelListRequest(communitySubchannelListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunitySubchannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunitySubchannels`: CommunitySubchannelListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunitySubchannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunitySubchannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communitySubchannelListRequest** | [**CommunitySubchannelListRequest**](CommunitySubchannelListRequest.md) |  | 

### Return type

[**CommunitySubchannelListResponse**](CommunitySubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityUserSubchannels

> CommunityUserSubchannelListResponse ListCommunityUserSubchannels(ctx).CommunityUserSubchannelListRequest(communityUserSubchannelListRequest).Execute()

List community user subchannels

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityUserSubchannelListRequest := *openapiclient.NewCommunityUserSubchannelListRequest("ChannelId_example", "UserId_example") // CommunityUserSubchannelListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListCommunityUserSubchannels(context.Background()).CommunityUserSubchannelListRequest(communityUserSubchannelListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListCommunityUserSubchannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityUserSubchannels`: CommunityUserSubchannelListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListCommunityUserSubchannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityUserSubchannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityUserSubchannelListRequest** | [**CommunityUserSubchannelListRequest**](CommunityUserSubchannelListRequest.md) |  | 

### Return type

[**CommunityUserSubchannelListResponse**](CommunityUserSubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPrivateSubchannelMembers

> CommunityPrivateSubchannelMemberListResponse ListPrivateSubchannelMembers(ctx).CommunityPrivateSubchannelMemberListRequest(communityPrivateSubchannelMemberListRequest).Execute()

List private subchannel members

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityPrivateSubchannelMemberListRequest := *openapiclient.NewCommunityPrivateSubchannelMemberListRequest("ChannelId_example", "SubchannelId_example") // CommunityPrivateSubchannelMemberListRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.ListPrivateSubchannelMembers(context.Background()).CommunityPrivateSubchannelMemberListRequest(communityPrivateSubchannelMemberListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.ListPrivateSubchannelMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPrivateSubchannelMembers`: CommunityPrivateSubchannelMemberListResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.ListPrivateSubchannelMembers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListPrivateSubchannelMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityPrivateSubchannelMemberListRequest** | [**CommunityPrivateSubchannelMemberListRequest**](CommunityPrivateSubchannelMemberListRequest.md) |  | 

### Return type

[**CommunityPrivateSubchannelMemberListResponse**](CommunityPrivateSubchannelMemberListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## QuitCommunityChannel

> CodeOnlyResponse QuitCommunityChannel(ctx).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()

Leave community channel

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelMemberRequest := *openapiclient.NewCommunityChannelMemberRequest("UserId_example", "ChannelId_example") // CommunityChannelMemberRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.QuitCommunityChannel(context.Background()).CommunityChannelMemberRequest(communityChannelMemberRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.QuitCommunityChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `QuitCommunityChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.QuitCommunityChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiQuitCommunityChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveCommunityChannelUserGroupUsers

> CodeOnlyResponse RemoveCommunityChannelUserGroupUsers(ctx).CommunityChannelUserGroupUsersRequest(communityChannelUserGroupUsersRequest).Execute()

Remove community channel user group users

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupUsersRequest := *openapiclient.NewCommunityChannelUserGroupUsersRequest("ChannelId_example", "UserGroupId_example", []string{"UserIds_example"}) // CommunityChannelUserGroupUsersRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.RemoveCommunityChannelUserGroupUsers(context.Background()).CommunityChannelUserGroupUsersRequest(communityChannelUserGroupUsersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.RemoveCommunityChannelUserGroupUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveCommunityChannelUserGroupUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.RemoveCommunityChannelUserGroupUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveCommunityChannelUserGroupUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupUsersRequest** | [**CommunityChannelUserGroupUsersRequest**](CommunityChannelUserGroupUsersRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveCommunityChannelUserGroups

> CodeOnlyResponse RemoveCommunityChannelUserGroups(ctx).CommunityChannelUserGroupDeleteRequest(communityChannelUserGroupDeleteRequest).Execute()

Delete community channel user groups

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupDeleteRequest := *openapiclient.NewCommunityChannelUserGroupDeleteRequest("ChannelId_example", []string{"UserGroupIds_example"}) // CommunityChannelUserGroupDeleteRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.RemoveCommunityChannelUserGroups(context.Background()).CommunityChannelUserGroupDeleteRequest(communityChannelUserGroupDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.RemoveCommunityChannelUserGroups``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveCommunityChannelUserGroups`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.RemoveCommunityChannelUserGroups`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveCommunityChannelUserGroupsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupDeleteRequest** | [**CommunityChannelUserGroupDeleteRequest**](CommunityChannelUserGroupDeleteRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemovePrivateSubchannelMembers

> CodeOnlyResponse RemovePrivateSubchannelMembers(ctx).CommunityPrivateSubchannelMembersRequest(communityPrivateSubchannelMembersRequest).Execute()

Remove private subchannel members

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityPrivateSubchannelMembersRequest := *openapiclient.NewCommunityPrivateSubchannelMembersRequest("ChannelId_example", "SubchannelId_example", []string{"UserIds_example"}) // CommunityPrivateSubchannelMembersRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.RemovePrivateSubchannelMembers(context.Background()).CommunityPrivateSubchannelMembersRequest(communityPrivateSubchannelMembersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.RemovePrivateSubchannelMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemovePrivateSubchannelMembers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.RemovePrivateSubchannelMembers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemovePrivateSubchannelMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityPrivateSubchannelMembersRequest** | [**CommunityPrivateSubchannelMembersRequest**](CommunityPrivateSubchannelMembersRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UnbindCommunityChannelUserGroup

> CodeOnlyResponse UnbindCommunityChannelUserGroup(ctx).CommunityChannelUserGroupBindingRequest(communityChannelUserGroupBindingRequest).Execute()

Unbind community channel user group

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUserGroupBindingRequest := *openapiclient.NewCommunityChannelUserGroupBindingRequest("ChannelId_example", "SubchannelId_example", []string{"UserGroupIds_example"}) // CommunityChannelUserGroupBindingRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.UnbindCommunityChannelUserGroup(context.Background()).CommunityChannelUserGroupBindingRequest(communityChannelUserGroupBindingRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.UnbindCommunityChannelUserGroup``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UnbindCommunityChannelUserGroup`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.UnbindCommunityChannelUserGroup`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUnbindCommunityChannelUserGroupRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUserGroupBindingRequest** | [**CommunityChannelUserGroupBindingRequest**](CommunityChannelUserGroupBindingRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateCommunityChannelInfo

> CodeOnlyResponse UpdateCommunityChannelInfo(ctx).CommunityChannelUpdateRequest(communityChannelUpdateRequest).Execute()

Update community channel info

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communityChannelUpdateRequest := *openapiclient.NewCommunityChannelUpdateRequest("ChannelId_example", "Name_example") // CommunityChannelUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.UpdateCommunityChannelInfo(context.Background()).CommunityChannelUpdateRequest(communityChannelUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.UpdateCommunityChannelInfo``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateCommunityChannelInfo`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.UpdateCommunityChannelInfo`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateCommunityChannelInfoRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelUpdateRequest** | [**CommunityChannelUpdateRequest**](CommunityChannelUpdateRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateCommunitySubchannelType

> CodeOnlyResponse UpdateCommunitySubchannelType(ctx).CommunitySubchannelTypeUpdateRequest(communitySubchannelTypeUpdateRequest).Execute()

Update community subchannel type

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "gitlab2.rongcloud.net/public-server/nexconn-server-sdk-go"
)

func main() {
	communitySubchannelTypeUpdateRequest := *openapiclient.NewCommunitySubchannelTypeUpdateRequest("ChannelId_example", "SubchannelId_example") // CommunitySubchannelTypeUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	configuration.SetRongCloudCredentials(
		os.Getenv("RONGCLOUD_APP_KEY"),
		os.Getenv("RONGCLOUD_APP_SECRET"),
	)
	if err := configuration.SetPrimaryBackupDomains(
		os.Getenv("RONGCLOUD_PRIMARY_API_DOMAIN"),
		os.Getenv("RONGCLOUD_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CommunityChannelManagementAPI.UpdateCommunitySubchannelType(context.Background()).CommunitySubchannelTypeUpdateRequest(communitySubchannelTypeUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelManagementAPI.UpdateCommunitySubchannelType``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateCommunitySubchannelType`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelManagementAPI.UpdateCommunitySubchannelType`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateCommunitySubchannelTypeRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communitySubchannelTypeUpdateRequest** | [**CommunitySubchannelTypeUpdateRequest**](CommunitySubchannelTypeUpdateRequest.md) |  | 

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


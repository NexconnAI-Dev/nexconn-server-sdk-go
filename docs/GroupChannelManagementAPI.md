# GroupChannelManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddGroupChannelAdmins**](GroupChannelManagementAPI.md#AddGroupChannelAdmins) | **Post** /v4/group-channel/admin/add | Add group admins
[**AddGroupChannelMemberFavorites**](GroupChannelManagementAPI.md#AddGroupChannelMemberFavorites) | **Post** /v4/group-channel/member/favorites/add | Add favorite group members
[**BatchGetGroupChannelMembers**](GroupChannelManagementAPI.md#BatchGetGroupChannelMembers) | **Post** /v4/group-channel/member/batch/get | Get specific group members
[**BatchGetGroupChannelProfiles**](GroupChannelManagementAPI.md#BatchGetGroupChannelProfiles) | **Post** /v4/group-channel/profile/list | List group profiles
[**CreateGroupChannel**](GroupChannelManagementAPI.md#CreateGroupChannel) | **Post** /v4/group-channel/create | Create a group
[**DeleteGroupChannelAlias**](GroupChannelManagementAPI.md#DeleteGroupChannelAlias) | **Post** /v4/group-channel/alias/delete | Delete group alias
[**DismissGroupChannel**](GroupChannelManagementAPI.md#DismissGroupChannel) | **Post** /v4/group-channel/dismiss | Dismiss a group
[**GetGroupChannelAlias**](GroupChannelManagementAPI.md#GetGroupChannelAlias) | **Post** /v4/group-channel/alias/get | Get group alias
[**JoinGroupChannel**](GroupChannelManagementAPI.md#JoinGroupChannel) | **Post** /v4/group-channel/join | Join a group
[**KickUserFromAllGroupChannels**](GroupChannelManagementAPI.md#KickUserFromAllGroupChannels) | **Post** /v4/group-channel/member/kickout-all | Remove a user from all groups
[**ListGroupChannelMemberFavorites**](GroupChannelManagementAPI.md#ListGroupChannelMemberFavorites) | **Post** /v4/group-channel/member/favorites/list | List favorite group members
[**ListGroupChannelMembers**](GroupChannelManagementAPI.md#ListGroupChannelMembers) | **Post** /v4/group-channel/member/list | Query group members
[**ListGroupChannels**](GroupChannelManagementAPI.md#ListGroupChannels) | **Post** /v4/group-channel/list | List group channels
[**ListUserJoinedGroupChannels**](GroupChannelManagementAPI.md#ListUserJoinedGroupChannels) | **Post** /v4/group-channel/joined/list | Query user&#39;s groups
[**QuitGroupChannel**](GroupChannelManagementAPI.md#QuitGroupChannel) | **Post** /v4/group-channel/leave | Leave a group
[**RemoveGroupChannelAdmins**](GroupChannelManagementAPI.md#RemoveGroupChannelAdmins) | **Post** /v4/group-channel/admin/remove | Remove group admins
[**RemoveGroupChannelMemberFavorites**](GroupChannelManagementAPI.md#RemoveGroupChannelMemberFavorites) | **Post** /v4/group-channel/member/favorites/remove | Remove favorite group members
[**SetGroupChannelAlias**](GroupChannelManagementAPI.md#SetGroupChannelAlias) | **Post** /v4/group-channel/alias/set | Set group alias
[**SetGroupChannelMember**](GroupChannelManagementAPI.md#SetGroupChannelMember) | **Post** /v4/group-channel/member/set | Set group member profile
[**TransferGroupChannelOwner**](GroupChannelManagementAPI.md#TransferGroupChannelOwner) | **Post** /v4/group-channel/transfer/owner | Transfer group ownership
[**UpdateGroupChannelProfile**](GroupChannelManagementAPI.md#UpdateGroupChannelProfile) | **Post** /v4/group-channel/profile/update | Update group info



## AddGroupChannelAdmins

> CodeOnlyResponse AddGroupChannelAdmins(ctx).GroupChannelAdminUsersRequest(groupChannelAdminUsersRequest).Execute()

Add group admins



### Example

```go
package main

import (
	"context"
	"fmt"
	"log"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelAdminUsersRequest := *openapiclient.NewGroupChannelAdminUsersRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelAdminUsersRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.AddGroupChannelAdmins(context.Background()).GroupChannelAdminUsersRequest(groupChannelAdminUsersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.AddGroupChannelAdmins``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddGroupChannelAdmins`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.AddGroupChannelAdmins`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddGroupChannelAdminsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAdminUsersRequest** | [**GroupChannelAdminUsersRequest**](GroupChannelAdminUsersRequest.md) |  | 

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


## AddGroupChannelMemberFavorites

> CodeOnlyResponse AddGroupChannelMemberFavorites(ctx).GroupChannelMemberFavoritesUpdateRequest(groupChannelMemberFavoritesUpdateRequest).Execute()

Add favorite group members



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberFavoritesUpdateRequest := *openapiclient.NewGroupChannelMemberFavoritesUpdateRequest("ChannelId_example", "UserId_example", []string{"FavoriteIds_example"}) // GroupChannelMemberFavoritesUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.AddGroupChannelMemberFavorites(context.Background()).GroupChannelMemberFavoritesUpdateRequest(groupChannelMemberFavoritesUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.AddGroupChannelMemberFavorites``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddGroupChannelMemberFavorites`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.AddGroupChannelMemberFavorites`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddGroupChannelMemberFavoritesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberFavoritesUpdateRequest** | [**GroupChannelMemberFavoritesUpdateRequest**](GroupChannelMemberFavoritesUpdateRequest.md) |  | 

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


## BatchGetGroupChannelMembers

> GroupChannelMemberBatchGetResponse BatchGetGroupChannelMembers(ctx).GroupChannelMemberBatchGetRequest(groupChannelMemberBatchGetRequest).Execute()

Get specific group members



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberBatchGetRequest := *openapiclient.NewGroupChannelMemberBatchGetRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelMemberBatchGetRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.BatchGetGroupChannelMembers(context.Background()).GroupChannelMemberBatchGetRequest(groupChannelMemberBatchGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.BatchGetGroupChannelMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchGetGroupChannelMembers`: GroupChannelMemberBatchGetResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.BatchGetGroupChannelMembers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchGetGroupChannelMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberBatchGetRequest** | [**GroupChannelMemberBatchGetRequest**](GroupChannelMemberBatchGetRequest.md) |  | 

### Return type

[**GroupChannelMemberBatchGetResponse**](GroupChannelMemberBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BatchGetGroupChannelProfiles

> GroupChannelProfileListResponse BatchGetGroupChannelProfiles(ctx).GroupChannelProfileListRequest(groupChannelProfileListRequest).Execute()

List group profiles



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelProfileListRequest := *openapiclient.NewGroupChannelProfileListRequest([]string{"ChannelIds_example"}) // GroupChannelProfileListRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.BatchGetGroupChannelProfiles(context.Background()).GroupChannelProfileListRequest(groupChannelProfileListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.BatchGetGroupChannelProfiles``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchGetGroupChannelProfiles`: GroupChannelProfileListResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.BatchGetGroupChannelProfiles`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchGetGroupChannelProfilesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelProfileListRequest** | [**GroupChannelProfileListRequest**](GroupChannelProfileListRequest.md) |  | 

### Return type

[**GroupChannelProfileListResponse**](GroupChannelProfileListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateGroupChannel

> CodeOnlyResponse CreateGroupChannel(ctx).GroupChannelCreateRequest(groupChannelCreateRequest).Execute()

Create a group



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelCreateRequest := *openapiclient.NewGroupChannelCreateRequest("ChannelId_example", "Name_example", "Owner_example") // GroupChannelCreateRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.CreateGroupChannel(context.Background()).GroupChannelCreateRequest(groupChannelCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.CreateGroupChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateGroupChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.CreateGroupChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateGroupChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelCreateRequest** | [**GroupChannelCreateRequest**](GroupChannelCreateRequest.md) |  | 

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


## DeleteGroupChannelAlias

> CodeOnlyResponse DeleteGroupChannelAlias(ctx).GroupChannelAliasGetRequest(groupChannelAliasGetRequest).Execute()

Delete group alias



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelAliasGetRequest := *openapiclient.NewGroupChannelAliasGetRequest("ChannelId_example", "UserId_example") // GroupChannelAliasGetRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.DeleteGroupChannelAlias(context.Background()).GroupChannelAliasGetRequest(groupChannelAliasGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.DeleteGroupChannelAlias``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteGroupChannelAlias`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.DeleteGroupChannelAlias`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteGroupChannelAliasRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAliasGetRequest** | [**GroupChannelAliasGetRequest**](GroupChannelAliasGetRequest.md) |  | 

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


## DismissGroupChannel

> CodeOnlyResponse DismissGroupChannel(ctx).GroupChannelDismissRequest(groupChannelDismissRequest).Execute()

Dismiss a group



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelDismissRequest := *openapiclient.NewGroupChannelDismissRequest("ChannelId_example") // GroupChannelDismissRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.DismissGroupChannel(context.Background()).GroupChannelDismissRequest(groupChannelDismissRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.DismissGroupChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DismissGroupChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.DismissGroupChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDismissGroupChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelDismissRequest** | [**GroupChannelDismissRequest**](GroupChannelDismissRequest.md) |  | 

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


## GetGroupChannelAlias

> GroupChannelAliasGetResponse GetGroupChannelAlias(ctx).GroupChannelAliasGetRequest(groupChannelAliasGetRequest).Execute()

Get group alias



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelAliasGetRequest := *openapiclient.NewGroupChannelAliasGetRequest("ChannelId_example", "UserId_example") // GroupChannelAliasGetRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.GetGroupChannelAlias(context.Background()).GroupChannelAliasGetRequest(groupChannelAliasGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.GetGroupChannelAlias``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetGroupChannelAlias`: GroupChannelAliasGetResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.GetGroupChannelAlias`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetGroupChannelAliasRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAliasGetRequest** | [**GroupChannelAliasGetRequest**](GroupChannelAliasGetRequest.md) |  | 

### Return type

[**GroupChannelAliasGetResponse**](GroupChannelAliasGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## JoinGroupChannel

> GroupChannelJoinResponse JoinGroupChannel(ctx).GroupChannelJoinRequest(groupChannelJoinRequest).Execute()

Join a group



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelJoinRequest := *openapiclient.NewGroupChannelJoinRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelJoinRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.JoinGroupChannel(context.Background()).GroupChannelJoinRequest(groupChannelJoinRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.JoinGroupChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `JoinGroupChannel`: GroupChannelJoinResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.JoinGroupChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiJoinGroupChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelJoinRequest** | [**GroupChannelJoinRequest**](GroupChannelJoinRequest.md) |  | 

### Return type

[**GroupChannelJoinResponse**](GroupChannelJoinResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## KickUserFromAllGroupChannels

> CodeOnlyResponse KickUserFromAllGroupChannels(ctx).GroupChannelKickUserFromAllRequest(groupChannelKickUserFromAllRequest).Execute()

Remove a user from all groups



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelKickUserFromAllRequest := *openapiclient.NewGroupChannelKickUserFromAllRequest("UserId_example") // GroupChannelKickUserFromAllRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.KickUserFromAllGroupChannels(context.Background()).GroupChannelKickUserFromAllRequest(groupChannelKickUserFromAllRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.KickUserFromAllGroupChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `KickUserFromAllGroupChannels`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.KickUserFromAllGroupChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiKickUserFromAllGroupChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelKickUserFromAllRequest** | [**GroupChannelKickUserFromAllRequest**](GroupChannelKickUserFromAllRequest.md) |  | 

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


## ListGroupChannelMemberFavorites

> GroupChannelMemberFavoritesListResponse ListGroupChannelMemberFavorites(ctx).GroupChannelMemberFavoritesListRequest(groupChannelMemberFavoritesListRequest).Execute()

List favorite group members



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberFavoritesListRequest := *openapiclient.NewGroupChannelMemberFavoritesListRequest("ChannelId_example", "UserId_example") // GroupChannelMemberFavoritesListRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.ListGroupChannelMemberFavorites(context.Background()).GroupChannelMemberFavoritesListRequest(groupChannelMemberFavoritesListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.ListGroupChannelMemberFavorites``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListGroupChannelMemberFavorites`: GroupChannelMemberFavoritesListResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.ListGroupChannelMemberFavorites`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListGroupChannelMemberFavoritesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberFavoritesListRequest** | [**GroupChannelMemberFavoritesListRequest**](GroupChannelMemberFavoritesListRequest.md) |  | 

### Return type

[**GroupChannelMemberFavoritesListResponse**](GroupChannelMemberFavoritesListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListGroupChannelMembers

> GroupChannelMemberListResponse ListGroupChannelMembers(ctx).GroupChannelMemberListRequest(groupChannelMemberListRequest).Execute()

Query group members



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberListRequest := *openapiclient.NewGroupChannelMemberListRequest("ChannelId_example") // GroupChannelMemberListRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.ListGroupChannelMembers(context.Background()).GroupChannelMemberListRequest(groupChannelMemberListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.ListGroupChannelMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListGroupChannelMembers`: GroupChannelMemberListResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.ListGroupChannelMembers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListGroupChannelMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberListRequest** | [**GroupChannelMemberListRequest**](GroupChannelMemberListRequest.md) |  | 

### Return type

[**GroupChannelMemberListResponse**](GroupChannelMemberListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListGroupChannels

> GroupChannelListResponse ListGroupChannels(ctx).GroupChannelListRequest(groupChannelListRequest).Execute()

List group channels



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelListRequest := *openapiclient.NewGroupChannelListRequest() // GroupChannelListRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.ListGroupChannels(context.Background()).GroupChannelListRequest(groupChannelListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.ListGroupChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListGroupChannels`: GroupChannelListResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.ListGroupChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListGroupChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelListRequest** | [**GroupChannelListRequest**](GroupChannelListRequest.md) |  | 

### Return type

[**GroupChannelListResponse**](GroupChannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListUserJoinedGroupChannels

> GroupChannelJoinedListResponse ListUserJoinedGroupChannels(ctx).GroupChannelJoinedListRequest(groupChannelJoinedListRequest).Execute()

Query user's groups



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelJoinedListRequest := *openapiclient.NewGroupChannelJoinedListRequest("UserId_example") // GroupChannelJoinedListRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.ListUserJoinedGroupChannels(context.Background()).GroupChannelJoinedListRequest(groupChannelJoinedListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.ListUserJoinedGroupChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListUserJoinedGroupChannels`: GroupChannelJoinedListResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.ListUserJoinedGroupChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListUserJoinedGroupChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelJoinedListRequest** | [**GroupChannelJoinedListRequest**](GroupChannelJoinedListRequest.md) |  | 

### Return type

[**GroupChannelJoinedListResponse**](GroupChannelJoinedListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## QuitGroupChannel

> CodeOnlyResponse QuitGroupChannel(ctx).GroupChannelQuitRequest(groupChannelQuitRequest).Execute()

Leave a group



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelQuitRequest := *openapiclient.NewGroupChannelQuitRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelQuitRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.QuitGroupChannel(context.Background()).GroupChannelQuitRequest(groupChannelQuitRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.QuitGroupChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `QuitGroupChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.QuitGroupChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiQuitGroupChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelQuitRequest** | [**GroupChannelQuitRequest**](GroupChannelQuitRequest.md) |  | 

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


## RemoveGroupChannelAdmins

> CodeOnlyResponse RemoveGroupChannelAdmins(ctx).GroupChannelAdminUsersRequest(groupChannelAdminUsersRequest).Execute()

Remove group admins



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelAdminUsersRequest := *openapiclient.NewGroupChannelAdminUsersRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelAdminUsersRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.RemoveGroupChannelAdmins(context.Background()).GroupChannelAdminUsersRequest(groupChannelAdminUsersRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.RemoveGroupChannelAdmins``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveGroupChannelAdmins`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.RemoveGroupChannelAdmins`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveGroupChannelAdminsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAdminUsersRequest** | [**GroupChannelAdminUsersRequest**](GroupChannelAdminUsersRequest.md) |  | 

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


## RemoveGroupChannelMemberFavorites

> CodeOnlyResponse RemoveGroupChannelMemberFavorites(ctx).GroupChannelMemberFavoritesUpdateRequest(groupChannelMemberFavoritesUpdateRequest).Execute()

Remove favorite group members



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberFavoritesUpdateRequest := *openapiclient.NewGroupChannelMemberFavoritesUpdateRequest("ChannelId_example", "UserId_example", []string{"FavoriteIds_example"}) // GroupChannelMemberFavoritesUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.RemoveGroupChannelMemberFavorites(context.Background()).GroupChannelMemberFavoritesUpdateRequest(groupChannelMemberFavoritesUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.RemoveGroupChannelMemberFavorites``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveGroupChannelMemberFavorites`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.RemoveGroupChannelMemberFavorites`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveGroupChannelMemberFavoritesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberFavoritesUpdateRequest** | [**GroupChannelMemberFavoritesUpdateRequest**](GroupChannelMemberFavoritesUpdateRequest.md) |  | 

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


## SetGroupChannelAlias

> CodeOnlyResponse SetGroupChannelAlias(ctx).GroupChannelAliasSetRequest(groupChannelAliasSetRequest).Execute()

Set group alias



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelAliasSetRequest := *openapiclient.NewGroupChannelAliasSetRequest("ChannelId_example", "UserId_example", "Alias_example") // GroupChannelAliasSetRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.SetGroupChannelAlias(context.Background()).GroupChannelAliasSetRequest(groupChannelAliasSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.SetGroupChannelAlias``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetGroupChannelAlias`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.SetGroupChannelAlias`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetGroupChannelAliasRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAliasSetRequest** | [**GroupChannelAliasSetRequest**](GroupChannelAliasSetRequest.md) |  | 

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


## SetGroupChannelMember

> CodeOnlyResponse SetGroupChannelMember(ctx).GroupChannelMemberSetRequest(groupChannelMemberSetRequest).Execute()

Set group member profile



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelMemberSetRequest := *openapiclient.NewGroupChannelMemberSetRequest("ChannelId_example", "UserId_example") // GroupChannelMemberSetRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.SetGroupChannelMember(context.Background()).GroupChannelMemberSetRequest(groupChannelMemberSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.SetGroupChannelMember``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetGroupChannelMember`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.SetGroupChannelMember`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetGroupChannelMemberRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMemberSetRequest** | [**GroupChannelMemberSetRequest**](GroupChannelMemberSetRequest.md) |  | 

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


## TransferGroupChannelOwner

> CodeOnlyResponse TransferGroupChannelOwner(ctx).GroupChannelTransferOwnerRequest(groupChannelTransferOwnerRequest).Execute()

Transfer group ownership



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelTransferOwnerRequest := *openapiclient.NewGroupChannelTransferOwnerRequest("ChannelId_example", "NewOwner_example") // GroupChannelTransferOwnerRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.TransferGroupChannelOwner(context.Background()).GroupChannelTransferOwnerRequest(groupChannelTransferOwnerRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.TransferGroupChannelOwner``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `TransferGroupChannelOwner`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.TransferGroupChannelOwner`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiTransferGroupChannelOwnerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelTransferOwnerRequest** | [**GroupChannelTransferOwnerRequest**](GroupChannelTransferOwnerRequest.md) |  | 

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


## UpdateGroupChannelProfile

> CodeOnlyResponse UpdateGroupChannelProfile(ctx).GroupChannelProfileUpdateRequest(groupChannelProfileUpdateRequest).Execute()

Update group info



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	groupChannelProfileUpdateRequest := *openapiclient.NewGroupChannelProfileUpdateRequest("ChannelId_example") // GroupChannelProfileUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelManagementAPI.UpdateGroupChannelProfile(context.Background()).GroupChannelProfileUpdateRequest(groupChannelProfileUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelManagementAPI.UpdateGroupChannelProfile``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateGroupChannelProfile`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelManagementAPI.UpdateGroupChannelProfile`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateGroupChannelProfileRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelProfileUpdateRequest** | [**GroupChannelProfileUpdateRequest**](GroupChannelProfileUpdateRequest.md) |  | 

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


# CommunityChannelModerationAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddCommunityChannelAllowedSenderList**](CommunityChannelModerationAPI.md#AddCommunityChannelAllowedSenderList) | **Post** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list
[**AddCommunityChannelMutedUsers**](CommunityChannelModerationAPI.md#AddCommunityChannelMutedUsers) | **Post** /v4/community-channel/mute-list/add | Add community-channel muted users
[**GetCommunityChannelFreezeList**](CommunityChannelModerationAPI.md#GetCommunityChannelFreezeList) | **Post** /v4/community-channel/freeze-list/get | Get community channel freeze status
[**ListCommunityChannelAllowedSenderList**](CommunityChannelModerationAPI.md#ListCommunityChannelAllowedSenderList) | **Post** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list
[**ListCommunityChannelMutedUsers**](CommunityChannelModerationAPI.md#ListCommunityChannelMutedUsers) | **Post** /v4/community-channel/mute-list/get | List community-channel muted users
[**RemoveCommunityChannelAllowedSenderList**](CommunityChannelModerationAPI.md#RemoveCommunityChannelAllowedSenderList) | **Post** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list
[**RemoveCommunityChannelMutedUsers**](CommunityChannelModerationAPI.md#RemoveCommunityChannelMutedUsers) | **Post** /v4/community-channel/mute-list/remove | Remove community-channel muted users
[**SetCommunityChannelFreezeList**](CommunityChannelModerationAPI.md#SetCommunityChannelFreezeList) | **Post** /v4/community-channel/freeze-list/set | Set community channel freeze list



## AddCommunityChannelAllowedSenderList

> CodeOnlyResponse AddCommunityChannelAllowedSenderList(ctx).CommunityChannelAllowedSenderListUpdateRequest(communityChannelAllowedSenderListUpdateRequest).Execute()

Add community channel allowed sender list

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
	communityChannelAllowedSenderListUpdateRequest := *openapiclient.NewCommunityChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"UserIds_example"}) // CommunityChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.AddCommunityChannelAllowedSenderList(context.Background()).CommunityChannelAllowedSenderListUpdateRequest(communityChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.AddCommunityChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddCommunityChannelAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.AddCommunityChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddCommunityChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelAllowedSenderListUpdateRequest** | [**CommunityChannelAllowedSenderListUpdateRequest**](CommunityChannelAllowedSenderListUpdateRequest.md) |  | 

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


## AddCommunityChannelMutedUsers

> CodeOnlyResponse AddCommunityChannelMutedUsers(ctx).CommunityChannelMuteListAddRequest(communityChannelMuteListAddRequest).Execute()

Add community-channel muted users

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
	communityChannelMuteListAddRequest := *openapiclient.NewCommunityChannelMuteListAddRequest("ChannelId_example", []string{"UserIds_example"}) // CommunityChannelMuteListAddRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.AddCommunityChannelMutedUsers(context.Background()).CommunityChannelMuteListAddRequest(communityChannelMuteListAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.AddCommunityChannelMutedUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddCommunityChannelMutedUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.AddCommunityChannelMutedUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddCommunityChannelMutedUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMuteListAddRequest** | [**CommunityChannelMuteListAddRequest**](CommunityChannelMuteListAddRequest.md) |  | 

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


## GetCommunityChannelFreezeList

> CommunityChannelFreezeListGetResponse GetCommunityChannelFreezeList(ctx).CommunityChannelFreezeListGetRequest(communityChannelFreezeListGetRequest).Execute()

Get community channel freeze status

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
	communityChannelFreezeListGetRequest := *openapiclient.NewCommunityChannelFreezeListGetRequest("ChannelId_example") // CommunityChannelFreezeListGetRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.GetCommunityChannelFreezeList(context.Background()).CommunityChannelFreezeListGetRequest(communityChannelFreezeListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.GetCommunityChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCommunityChannelFreezeList`: CommunityChannelFreezeListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.GetCommunityChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetCommunityChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelFreezeListGetRequest** | [**CommunityChannelFreezeListGetRequest**](CommunityChannelFreezeListGetRequest.md) |  | 

### Return type

[**CommunityChannelFreezeListGetResponse**](CommunityChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelAllowedSenderList

> CommunityChannelAllowedSenderListGetResponse ListCommunityChannelAllowedSenderList(ctx).CommunityChannelAllowedSenderListGetRequest(communityChannelAllowedSenderListGetRequest).Execute()

List community channel allowed sender list

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
	communityChannelAllowedSenderListGetRequest := *openapiclient.NewCommunityChannelAllowedSenderListGetRequest("ChannelId_example") // CommunityChannelAllowedSenderListGetRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.ListCommunityChannelAllowedSenderList(context.Background()).CommunityChannelAllowedSenderListGetRequest(communityChannelAllowedSenderListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.ListCommunityChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelAllowedSenderList`: CommunityChannelAllowedSenderListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.ListCommunityChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelAllowedSenderListGetRequest** | [**CommunityChannelAllowedSenderListGetRequest**](CommunityChannelAllowedSenderListGetRequest.md) |  | 

### Return type

[**CommunityChannelAllowedSenderListGetResponse**](CommunityChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelMutedUsers

> CommunityChannelMuteListGetResponse ListCommunityChannelMutedUsers(ctx).CommunityChannelMuteListGetRequest(communityChannelMuteListGetRequest).Execute()

List community-channel muted users

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
	communityChannelMuteListGetRequest := *openapiclient.NewCommunityChannelMuteListGetRequest("ChannelId_example") // CommunityChannelMuteListGetRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.ListCommunityChannelMutedUsers(context.Background()).CommunityChannelMuteListGetRequest(communityChannelMuteListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.ListCommunityChannelMutedUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelMutedUsers`: CommunityChannelMuteListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.ListCommunityChannelMutedUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelMutedUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMuteListGetRequest** | [**CommunityChannelMuteListGetRequest**](CommunityChannelMuteListGetRequest.md) |  | 

### Return type

[**CommunityChannelMuteListGetResponse**](CommunityChannelMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveCommunityChannelAllowedSenderList

> CodeOnlyResponse RemoveCommunityChannelAllowedSenderList(ctx).CommunityChannelAllowedSenderListUpdateRequest(communityChannelAllowedSenderListUpdateRequest).Execute()

Remove community channel allowed sender list

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
	communityChannelAllowedSenderListUpdateRequest := *openapiclient.NewCommunityChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"UserIds_example"}) // CommunityChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.RemoveCommunityChannelAllowedSenderList(context.Background()).CommunityChannelAllowedSenderListUpdateRequest(communityChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.RemoveCommunityChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveCommunityChannelAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.RemoveCommunityChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveCommunityChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelAllowedSenderListUpdateRequest** | [**CommunityChannelAllowedSenderListUpdateRequest**](CommunityChannelAllowedSenderListUpdateRequest.md) |  | 

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


## RemoveCommunityChannelMutedUsers

> CodeOnlyResponse RemoveCommunityChannelMutedUsers(ctx).CommunityChannelMuteListRemoveRequest(communityChannelMuteListRemoveRequest).Execute()

Remove community-channel muted users

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
	communityChannelMuteListRemoveRequest := *openapiclient.NewCommunityChannelMuteListRemoveRequest("ChannelId_example", []string{"UserIds_example"}) // CommunityChannelMuteListRemoveRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.RemoveCommunityChannelMutedUsers(context.Background()).CommunityChannelMuteListRemoveRequest(communityChannelMuteListRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.RemoveCommunityChannelMutedUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveCommunityChannelMutedUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.RemoveCommunityChannelMutedUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveCommunityChannelMutedUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMuteListRemoveRequest** | [**CommunityChannelMuteListRemoveRequest**](CommunityChannelMuteListRemoveRequest.md) |  | 

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


## SetCommunityChannelFreezeList

> CodeOnlyResponse SetCommunityChannelFreezeList(ctx).CommunityChannelFreezeListSetRequest(communityChannelFreezeListSetRequest).Execute()

Set community channel freeze list

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
	communityChannelFreezeListSetRequest := *openapiclient.NewCommunityChannelFreezeListSetRequest("ChannelId_example", false) // CommunityChannelFreezeListSetRequest | 

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
	resp, r, err := apiClient.CommunityChannelModerationAPI.SetCommunityChannelFreezeList(context.Background()).CommunityChannelFreezeListSetRequest(communityChannelFreezeListSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CommunityChannelModerationAPI.SetCommunityChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetCommunityChannelFreezeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `CommunityChannelModerationAPI.SetCommunityChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetCommunityChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelFreezeListSetRequest** | [**CommunityChannelFreezeListSetRequest**](CommunityChannelFreezeListSetRequest.md) |  | 

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


# GroupChannelModerationAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddGroupChannelAllowedSenderList**](GroupChannelModerationAPI.md#AddGroupChannelAllowedSenderList) | **Post** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list
[**AddGroupChannelFreezeList**](GroupChannelModerationAPI.md#AddGroupChannelFreezeList) | **Post** /v4/group-channel/freeze-list/add | Freeze a group
[**AddGroupChannelUserMuteList**](GroupChannelModerationAPI.md#AddGroupChannelUserMuteList) | **Post** /v4/group-channel/user/mute-list/add | Mute a group member
[**GetGroupChannelAllowedSenderList**](GroupChannelModerationAPI.md#GetGroupChannelAllowedSenderList) | **Post** /v4/group-channel/allowed-sender-list/get | Query allowed senders list
[**GetGroupChannelFreezeList**](GroupChannelModerationAPI.md#GetGroupChannelFreezeList) | **Post** /v4/group-channel/freeze-list/get | Query group freeze status
[**GetGroupChannelUserMuteList**](GroupChannelModerationAPI.md#GetGroupChannelUserMuteList) | **Post** /v4/group-channel/user/mute-list/get | List muted group members
[**RemoveGroupChannelAllowedSenderList**](GroupChannelModerationAPI.md#RemoveGroupChannelAllowedSenderList) | **Post** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list
[**RemoveGroupChannelFreezeList**](GroupChannelModerationAPI.md#RemoveGroupChannelFreezeList) | **Post** /v4/group-channel/freeze-list/remove | Unfreeze a group
[**RemoveGroupChannelUserMuteList**](GroupChannelModerationAPI.md#RemoveGroupChannelUserMuteList) | **Post** /v4/group-channel/user/mute-list/remove | Unmute a group member



## AddGroupChannelAllowedSenderList

> CodeOnlyResponse AddGroupChannelAllowedSenderList(ctx).GroupChannelAllowedSenderListUpdateRequest(groupChannelAllowedSenderListUpdateRequest).Execute()

Add to allowed senders list



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
	groupChannelAllowedSenderListUpdateRequest := *openapiclient.NewGroupChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.AddGroupChannelAllowedSenderList(context.Background()).GroupChannelAllowedSenderListUpdateRequest(groupChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.AddGroupChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddGroupChannelAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.AddGroupChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddGroupChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAllowedSenderListUpdateRequest** | [**GroupChannelAllowedSenderListUpdateRequest**](GroupChannelAllowedSenderListUpdateRequest.md) |  | 

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


## AddGroupChannelFreezeList

> CodeOnlyResponse AddGroupChannelFreezeList(ctx).GroupChannelFreezeListUpdateRequest(groupChannelFreezeListUpdateRequest).Execute()

Freeze a group



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
	groupChannelFreezeListUpdateRequest := *openapiclient.NewGroupChannelFreezeListUpdateRequest([]string{"ChannelIds_example"}) // GroupChannelFreezeListUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.AddGroupChannelFreezeList(context.Background()).GroupChannelFreezeListUpdateRequest(groupChannelFreezeListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.AddGroupChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddGroupChannelFreezeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.AddGroupChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddGroupChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelFreezeListUpdateRequest** | [**GroupChannelFreezeListUpdateRequest**](GroupChannelFreezeListUpdateRequest.md) |  | 

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


## AddGroupChannelUserMuteList

> CodeOnlyResponse AddGroupChannelUserMuteList(ctx).GroupChannelUserMuteListAddRequest(groupChannelUserMuteListAddRequest).Execute()

Mute a group member



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
	groupChannelUserMuteListAddRequest := *openapiclient.NewGroupChannelUserMuteListAddRequest([]string{"UserIds_example"}, int32(123)) // GroupChannelUserMuteListAddRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.AddGroupChannelUserMuteList(context.Background()).GroupChannelUserMuteListAddRequest(groupChannelUserMuteListAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.AddGroupChannelUserMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddGroupChannelUserMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.AddGroupChannelUserMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddGroupChannelUserMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelUserMuteListAddRequest** | [**GroupChannelUserMuteListAddRequest**](GroupChannelUserMuteListAddRequest.md) |  | 

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


## GetGroupChannelAllowedSenderList

> GroupChannelAllowedSenderListGetResponse GetGroupChannelAllowedSenderList(ctx).GroupChannelAllowedSenderListGetRequest(groupChannelAllowedSenderListGetRequest).Execute()

Query allowed senders list



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
	groupChannelAllowedSenderListGetRequest := *openapiclient.NewGroupChannelAllowedSenderListGetRequest("ChannelId_example") // GroupChannelAllowedSenderListGetRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.GetGroupChannelAllowedSenderList(context.Background()).GroupChannelAllowedSenderListGetRequest(groupChannelAllowedSenderListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.GetGroupChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetGroupChannelAllowedSenderList`: GroupChannelAllowedSenderListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.GetGroupChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetGroupChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAllowedSenderListGetRequest** | [**GroupChannelAllowedSenderListGetRequest**](GroupChannelAllowedSenderListGetRequest.md) |  | 

### Return type

[**GroupChannelAllowedSenderListGetResponse**](GroupChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetGroupChannelFreezeList

> GroupChannelFreezeListGetResponse GetGroupChannelFreezeList(ctx).GroupChannelFreezeListGetRequest(groupChannelFreezeListGetRequest).Execute()

Query group freeze status



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
	groupChannelFreezeListGetRequest := *openapiclient.NewGroupChannelFreezeListGetRequest() // GroupChannelFreezeListGetRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.GetGroupChannelFreezeList(context.Background()).GroupChannelFreezeListGetRequest(groupChannelFreezeListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.GetGroupChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetGroupChannelFreezeList`: GroupChannelFreezeListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.GetGroupChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetGroupChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelFreezeListGetRequest** | [**GroupChannelFreezeListGetRequest**](GroupChannelFreezeListGetRequest.md) |  | 

### Return type

[**GroupChannelFreezeListGetResponse**](GroupChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetGroupChannelUserMuteList

> GroupChannelUserMuteListGetResponse GetGroupChannelUserMuteList(ctx).GroupChannelUserMuteListGetRequest(groupChannelUserMuteListGetRequest).Execute()

List muted group members



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
	groupChannelUserMuteListGetRequest := *openapiclient.NewGroupChannelUserMuteListGetRequest() // GroupChannelUserMuteListGetRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.GetGroupChannelUserMuteList(context.Background()).GroupChannelUserMuteListGetRequest(groupChannelUserMuteListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.GetGroupChannelUserMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetGroupChannelUserMuteList`: GroupChannelUserMuteListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.GetGroupChannelUserMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetGroupChannelUserMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelUserMuteListGetRequest** | [**GroupChannelUserMuteListGetRequest**](GroupChannelUserMuteListGetRequest.md) |  | 

### Return type

[**GroupChannelUserMuteListGetResponse**](GroupChannelUserMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveGroupChannelAllowedSenderList

> CodeOnlyResponse RemoveGroupChannelAllowedSenderList(ctx).GroupChannelAllowedSenderListUpdateRequest(groupChannelAllowedSenderListUpdateRequest).Execute()

Remove from allowed senders list



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
	groupChannelAllowedSenderListUpdateRequest := *openapiclient.NewGroupChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"UserIds_example"}) // GroupChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.RemoveGroupChannelAllowedSenderList(context.Background()).GroupChannelAllowedSenderListUpdateRequest(groupChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.RemoveGroupChannelAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveGroupChannelAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.RemoveGroupChannelAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveGroupChannelAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelAllowedSenderListUpdateRequest** | [**GroupChannelAllowedSenderListUpdateRequest**](GroupChannelAllowedSenderListUpdateRequest.md) |  | 

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


## RemoveGroupChannelFreezeList

> CodeOnlyResponse RemoveGroupChannelFreezeList(ctx).GroupChannelFreezeListUpdateRequest(groupChannelFreezeListUpdateRequest).Execute()

Unfreeze a group



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
	groupChannelFreezeListUpdateRequest := *openapiclient.NewGroupChannelFreezeListUpdateRequest([]string{"ChannelIds_example"}) // GroupChannelFreezeListUpdateRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.RemoveGroupChannelFreezeList(context.Background()).GroupChannelFreezeListUpdateRequest(groupChannelFreezeListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.RemoveGroupChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveGroupChannelFreezeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.RemoveGroupChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveGroupChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelFreezeListUpdateRequest** | [**GroupChannelFreezeListUpdateRequest**](GroupChannelFreezeListUpdateRequest.md) |  | 

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


## RemoveGroupChannelUserMuteList

> CodeOnlyResponse RemoveGroupChannelUserMuteList(ctx).GroupChannelUserMuteListRemoveRequest(groupChannelUserMuteListRemoveRequest).Execute()

Unmute a group member



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
	groupChannelUserMuteListRemoveRequest := *openapiclient.NewGroupChannelUserMuteListRemoveRequest([]string{"UserIds_example"}) // GroupChannelUserMuteListRemoveRequest | 

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
	resp, r, err := apiClient.GroupChannelModerationAPI.RemoveGroupChannelUserMuteList(context.Background()).GroupChannelUserMuteListRemoveRequest(groupChannelUserMuteListRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GroupChannelModerationAPI.RemoveGroupChannelUserMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveGroupChannelUserMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `GroupChannelModerationAPI.RemoveGroupChannelUserMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveGroupChannelUserMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelUserMuteListRemoveRequest** | [**GroupChannelUserMuteListRemoveRequest**](GroupChannelUserMuteListRemoveRequest.md) |  | 

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


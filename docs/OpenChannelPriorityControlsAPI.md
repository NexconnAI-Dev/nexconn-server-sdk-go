# OpenChannelPriorityControlsAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsAPI.md#AddOpenChannelPriorityMessageTypeList) | **Post** /v4/open-channel/priority-message-type-list/add | Add priority message types
[**AddOpenChannelPrioritySenderList**](OpenChannelPriorityControlsAPI.md#AddOpenChannelPrioritySenderList) | **Post** /v4/open-channel/priority-sender-list/add | Add priority senders
[**GetOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsAPI.md#GetOpenChannelPriorityMessageTypeList) | **Post** /v4/open-channel/priority-message-type-list/get | Query priority message types
[**GetOpenChannelPrioritySenderList**](OpenChannelPriorityControlsAPI.md#GetOpenChannelPrioritySenderList) | **Post** /v4/open-channel/priority-sender-list/get | Query priority senders
[**RemoveOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsAPI.md#RemoveOpenChannelPriorityMessageTypeList) | **Post** /v4/open-channel/priority-message-type-list/remove | Remove priority message types
[**RemoveOpenChannelPrioritySenderList**](OpenChannelPriorityControlsAPI.md#RemoveOpenChannelPrioritySenderList) | **Post** /v4/open-channel/priority-sender-list/remove | Remove priority senders



## AddOpenChannelPriorityMessageTypeList

> CodeOnlyResponse AddOpenChannelPriorityMessageTypeList(ctx).OpenChannelPriorityMessageTypeListRequest(openChannelPriorityMessageTypeListRequest).Execute()

Add priority message types



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
	openChannelPriorityMessageTypeListRequest := *openapiclient.NewOpenChannelPriorityMessageTypeListRequest([]string{"MessageTypes_example"}) // OpenChannelPriorityMessageTypeListRequest | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.AddOpenChannelPriorityMessageTypeList(context.Background()).OpenChannelPriorityMessageTypeListRequest(openChannelPriorityMessageTypeListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.AddOpenChannelPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelPriorityMessageTypeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.AddOpenChannelPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelPriorityMessageTypeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelPriorityMessageTypeListRequest** | [**OpenChannelPriorityMessageTypeListRequest**](OpenChannelPriorityMessageTypeListRequest.md) |  | 

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


## AddOpenChannelPrioritySenderList

> CodeOnlyResponse AddOpenChannelPrioritySenderList(ctx).OpenChannelParticipantIdsRequest(openChannelParticipantIdsRequest).Execute()

Add priority senders



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
	openChannelParticipantIdsRequest := *openapiclient.NewOpenChannelParticipantIdsRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelParticipantIdsRequest | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.AddOpenChannelPrioritySenderList(context.Background()).OpenChannelParticipantIdsRequest(openChannelParticipantIdsRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.AddOpenChannelPrioritySenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelPrioritySenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.AddOpenChannelPrioritySenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelPrioritySenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantIdsRequest** | [**OpenChannelParticipantIdsRequest**](OpenChannelParticipantIdsRequest.md) |  | 

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


## GetOpenChannelPriorityMessageTypeList

> OpenChannelMessageTypeListResponse GetOpenChannelPriorityMessageTypeList(ctx).Body(body).Execute()

Query priority message types



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
	body := map[string]interface{}{ ... } // map[string]interface{} | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.GetOpenChannelPriorityMessageTypeList(context.Background()).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.GetOpenChannelPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelPriorityMessageTypeList`: OpenChannelMessageTypeListResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.GetOpenChannelPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelPriorityMessageTypeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **map[string]interface{}** |  | 

### Return type

[**OpenChannelMessageTypeListResponse**](OpenChannelMessageTypeListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetOpenChannelPrioritySenderList

> OpenChannelParticipantIdsResponse GetOpenChannelPrioritySenderList(ctx).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()

Query priority senders



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
	openChannelParticipantListByChannelRequest := *openapiclient.NewOpenChannelParticipantListByChannelRequest("ChannelId_example") // OpenChannelParticipantListByChannelRequest | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.GetOpenChannelPrioritySenderList(context.Background()).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.GetOpenChannelPrioritySenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelPrioritySenderList`: OpenChannelParticipantIdsResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.GetOpenChannelPrioritySenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelPrioritySenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantListByChannelRequest** | [**OpenChannelParticipantListByChannelRequest**](OpenChannelParticipantListByChannelRequest.md) |  | 

### Return type

[**OpenChannelParticipantIdsResponse**](OpenChannelParticipantIdsResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveOpenChannelPriorityMessageTypeList

> CodeOnlyResponse RemoveOpenChannelPriorityMessageTypeList(ctx).OpenChannelPriorityMessageTypeListRequest(openChannelPriorityMessageTypeListRequest).Execute()

Remove priority message types



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
	openChannelPriorityMessageTypeListRequest := *openapiclient.NewOpenChannelPriorityMessageTypeListRequest([]string{"MessageTypes_example"}) // OpenChannelPriorityMessageTypeListRequest | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.RemoveOpenChannelPriorityMessageTypeList(context.Background()).OpenChannelPriorityMessageTypeListRequest(openChannelPriorityMessageTypeListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.RemoveOpenChannelPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelPriorityMessageTypeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.RemoveOpenChannelPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelPriorityMessageTypeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelPriorityMessageTypeListRequest** | [**OpenChannelPriorityMessageTypeListRequest**](OpenChannelPriorityMessageTypeListRequest.md) |  | 

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


## RemoveOpenChannelPrioritySenderList

> CodeOnlyResponse RemoveOpenChannelPrioritySenderList(ctx).OpenChannelParticipantIdsRequest(openChannelParticipantIdsRequest).Execute()

Remove priority senders



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
	openChannelParticipantIdsRequest := *openapiclient.NewOpenChannelParticipantIdsRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelParticipantIdsRequest | 

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
	resp, r, err := apiClient.OpenChannelPriorityControlsAPI.RemoveOpenChannelPrioritySenderList(context.Background()).OpenChannelParticipantIdsRequest(openChannelParticipantIdsRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelPriorityControlsAPI.RemoveOpenChannelPrioritySenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelPrioritySenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelPriorityControlsAPI.RemoveOpenChannelPrioritySenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelPrioritySenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantIdsRequest** | [**OpenChannelParticipantIdsRequest**](OpenChannelParticipantIdsRequest.md) |  | 

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


# OpenChannelMessagePriorityAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityAPI.md#AddOpenChannelLowPriorityMessageTypeList) | **Post** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types
[**GetOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityAPI.md#GetOpenChannelLowPriorityMessageTypeList) | **Post** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types
[**RemoveOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityAPI.md#RemoveOpenChannelLowPriorityMessageTypeList) | **Post** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types



## AddOpenChannelLowPriorityMessageTypeList

> CodeOnlyResponse AddOpenChannelLowPriorityMessageTypeList(ctx).OpenChannelLowPriorityMessageTypeListRequest(openChannelLowPriorityMessageTypeListRequest).Execute()

Add low-priority message types



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
	openChannelLowPriorityMessageTypeListRequest := *openapiclient.NewOpenChannelLowPriorityMessageTypeListRequest([]string{"MessageTypes_example"}) // OpenChannelLowPriorityMessageTypeListRequest | 

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
	resp, r, err := apiClient.OpenChannelMessagePriorityAPI.AddOpenChannelLowPriorityMessageTypeList(context.Background()).OpenChannelLowPriorityMessageTypeListRequest(openChannelLowPriorityMessageTypeListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMessagePriorityAPI.AddOpenChannelLowPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelLowPriorityMessageTypeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMessagePriorityAPI.AddOpenChannelLowPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelLowPriorityMessageTypeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelLowPriorityMessageTypeListRequest** | [**OpenChannelLowPriorityMessageTypeListRequest**](OpenChannelLowPriorityMessageTypeListRequest.md) |  | 

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


## GetOpenChannelLowPriorityMessageTypeList

> OpenChannelMessageTypeListResponse GetOpenChannelLowPriorityMessageTypeList(ctx).Body(body).Execute()

Query low-priority message types



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
	resp, r, err := apiClient.OpenChannelMessagePriorityAPI.GetOpenChannelLowPriorityMessageTypeList(context.Background()).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMessagePriorityAPI.GetOpenChannelLowPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelLowPriorityMessageTypeList`: OpenChannelMessageTypeListResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMessagePriorityAPI.GetOpenChannelLowPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelLowPriorityMessageTypeListRequest struct via the builder pattern


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


## RemoveOpenChannelLowPriorityMessageTypeList

> CodeOnlyResponse RemoveOpenChannelLowPriorityMessageTypeList(ctx).OpenChannelLowPriorityMessageTypeListRequest(openChannelLowPriorityMessageTypeListRequest).Execute()

Remove low-priority message types



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
	openChannelLowPriorityMessageTypeListRequest := *openapiclient.NewOpenChannelLowPriorityMessageTypeListRequest([]string{"MessageTypes_example"}) // OpenChannelLowPriorityMessageTypeListRequest | 

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
	resp, r, err := apiClient.OpenChannelMessagePriorityAPI.RemoveOpenChannelLowPriorityMessageTypeList(context.Background()).OpenChannelLowPriorityMessageTypeListRequest(openChannelLowPriorityMessageTypeListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMessagePriorityAPI.RemoveOpenChannelLowPriorityMessageTypeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelLowPriorityMessageTypeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMessagePriorityAPI.RemoveOpenChannelLowPriorityMessageTypeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelLowPriorityMessageTypeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelLowPriorityMessageTypeListRequest** | [**OpenChannelLowPriorityMessageTypeListRequest**](OpenChannelLowPriorityMessageTypeListRequest.md) |  | 

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


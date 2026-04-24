# OpenChannelManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateOpenChannel**](OpenChannelManagementAPI.md#CreateOpenChannel) | **Post** /v4/open-channel/create | Create an open channel
[**DestroyOpenChannels**](OpenChannelManagementAPI.md#DestroyOpenChannels) | **Post** /v4/open-channel/destroy | Destroy an open channel
[**GetOpenChannel**](OpenChannelManagementAPI.md#GetOpenChannel) | **Post** /v4/open-channel/get | Get open channel info
[**SetOpenChannelDestroyType**](OpenChannelManagementAPI.md#SetOpenChannelDestroyType) | **Post** /v4/open-channel/destroy-type/set | Set auto-destroy type



## CreateOpenChannel

> CodeOnlyResponse CreateOpenChannel(ctx).OpenChannelCreateRequest(openChannelCreateRequest).Execute()

Create an open channel



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
	openChannelCreateRequest := *openapiclient.NewOpenChannelCreateRequest("ChannelId_example") // OpenChannelCreateRequest | 

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
	resp, r, err := apiClient.OpenChannelManagementAPI.CreateOpenChannel(context.Background()).OpenChannelCreateRequest(openChannelCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelManagementAPI.CreateOpenChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateOpenChannel`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelManagementAPI.CreateOpenChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateOpenChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelCreateRequest** | [**OpenChannelCreateRequest**](OpenChannelCreateRequest.md) |  | 

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


## DestroyOpenChannels

> CodeOnlyResponse DestroyOpenChannels(ctx).OpenChannelDestroyRequest(openChannelDestroyRequest).Execute()

Destroy an open channel



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
	openChannelDestroyRequest := *openapiclient.NewOpenChannelDestroyRequest([]string{"ChannelIds_example"}) // OpenChannelDestroyRequest | 

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
	resp, r, err := apiClient.OpenChannelManagementAPI.DestroyOpenChannels(context.Background()).OpenChannelDestroyRequest(openChannelDestroyRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelManagementAPI.DestroyOpenChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DestroyOpenChannels`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelManagementAPI.DestroyOpenChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDestroyOpenChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelDestroyRequest** | [**OpenChannelDestroyRequest**](OpenChannelDestroyRequest.md) |  | 

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


## GetOpenChannel

> OpenChannelGetResponse GetOpenChannel(ctx).OpenChannelGetRequest(openChannelGetRequest).Execute()

Get open channel info



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
	openChannelGetRequest := *openapiclient.NewOpenChannelGetRequest("ChannelId_example") // OpenChannelGetRequest | 

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
	resp, r, err := apiClient.OpenChannelManagementAPI.GetOpenChannel(context.Background()).OpenChannelGetRequest(openChannelGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelManagementAPI.GetOpenChannel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannel`: OpenChannelGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelManagementAPI.GetOpenChannel`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelGetRequest** | [**OpenChannelGetRequest**](OpenChannelGetRequest.md) |  | 

### Return type

[**OpenChannelGetResponse**](OpenChannelGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SetOpenChannelDestroyType

> CodeOnlyResponse SetOpenChannelDestroyType(ctx).OpenChannelDestroyTypeSetRequest(openChannelDestroyTypeSetRequest).Execute()

Set auto-destroy type



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
	openChannelDestroyTypeSetRequest := *openapiclient.NewOpenChannelDestroyTypeSetRequest("ChannelId_example") // OpenChannelDestroyTypeSetRequest | 

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
	resp, r, err := apiClient.OpenChannelManagementAPI.SetOpenChannelDestroyType(context.Background()).OpenChannelDestroyTypeSetRequest(openChannelDestroyTypeSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelManagementAPI.SetOpenChannelDestroyType``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetOpenChannelDestroyType`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelManagementAPI.SetOpenChannelDestroyType`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetOpenChannelDestroyTypeRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelDestroyTypeSetRequest** | [**OpenChannelDestroyTypeSetRequest**](OpenChannelDestroyTypeSetRequest.md) |  | 

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


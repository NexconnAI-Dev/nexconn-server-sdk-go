# OpenChannelMetadataAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BatchGetOpenChannelMetadata**](OpenChannelMetadataAPI.md#BatchGetOpenChannelMetadata) | **Post** /v4/open-channel/metadata/batch/get | Query metadata
[**BatchRemoveOpenChannelMetadata**](OpenChannelMetadataAPI.md#BatchRemoveOpenChannelMetadata) | **Post** /v4/open-channel/metadata/batch/remove | Batch delete metadata
[**BatchSetOpenChannelMetadata**](OpenChannelMetadataAPI.md#BatchSetOpenChannelMetadata) | **Post** /v4/open-channel/metadata/batch/set | Batch set metadata



## BatchGetOpenChannelMetadata

> OpenChannelMetadataBatchGetResponse BatchGetOpenChannelMetadata(ctx).OpenChannelMetadataBatchGetRequest(openChannelMetadataBatchGetRequest).Execute()

Query metadata



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
	openChannelMetadataBatchGetRequest := *openapiclient.NewOpenChannelMetadataBatchGetRequest("ChannelId_example") // OpenChannelMetadataBatchGetRequest | 

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
	resp, r, err := apiClient.OpenChannelMetadataAPI.BatchGetOpenChannelMetadata(context.Background()).OpenChannelMetadataBatchGetRequest(openChannelMetadataBatchGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMetadataAPI.BatchGetOpenChannelMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchGetOpenChannelMetadata`: OpenChannelMetadataBatchGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMetadataAPI.BatchGetOpenChannelMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchGetOpenChannelMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelMetadataBatchGetRequest** | [**OpenChannelMetadataBatchGetRequest**](OpenChannelMetadataBatchGetRequest.md) |  | 

### Return type

[**OpenChannelMetadataBatchGetResponse**](OpenChannelMetadataBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BatchRemoveOpenChannelMetadata

> CodeOnlyResponse BatchRemoveOpenChannelMetadata(ctx).OpenChannelMetadataBatchRemoveRequest(openChannelMetadataBatchRemoveRequest).Execute()

Batch delete metadata



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
	openChannelMetadataBatchRemoveRequest := *openapiclient.NewOpenChannelMetadataBatchRemoveRequest("ChannelId_example", "MetadataOwnerId_example", []string{"MetadataKeys_example"}) // OpenChannelMetadataBatchRemoveRequest | 

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
	resp, r, err := apiClient.OpenChannelMetadataAPI.BatchRemoveOpenChannelMetadata(context.Background()).OpenChannelMetadataBatchRemoveRequest(openChannelMetadataBatchRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMetadataAPI.BatchRemoveOpenChannelMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchRemoveOpenChannelMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMetadataAPI.BatchRemoveOpenChannelMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchRemoveOpenChannelMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelMetadataBatchRemoveRequest** | [**OpenChannelMetadataBatchRemoveRequest**](OpenChannelMetadataBatchRemoveRequest.md) |  | 

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


## BatchSetOpenChannelMetadata

> CodeOnlyResponse BatchSetOpenChannelMetadata(ctx).OpenChannelMetadataBatchSetRequest(openChannelMetadataBatchSetRequest).Execute()

Batch set metadata



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
	openChannelMetadataBatchSetRequest := *openapiclient.NewOpenChannelMetadataBatchSetRequest("ChannelId_example", "MetadataOwnerId_example", map[string]string{"key": "Inner_example"}) // OpenChannelMetadataBatchSetRequest | 

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
	resp, r, err := apiClient.OpenChannelMetadataAPI.BatchSetOpenChannelMetadata(context.Background()).OpenChannelMetadataBatchSetRequest(openChannelMetadataBatchSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelMetadataAPI.BatchSetOpenChannelMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchSetOpenChannelMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelMetadataAPI.BatchSetOpenChannelMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchSetOpenChannelMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelMetadataBatchSetRequest** | [**OpenChannelMetadataBatchSetRequest**](OpenChannelMetadataBatchSetRequest.md) |  | 

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


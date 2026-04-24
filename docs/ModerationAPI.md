# ModerationAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BatchAddProfanityWords**](ModerationAPI.md#BatchAddProfanityWords) | **Post** /v4/profanity-word/batch/add | Batch add profanity words
[**BatchRemoveProfanityWords**](ModerationAPI.md#BatchRemoveProfanityWords) | **Post** /v4/profanity-word/batch/remove | Batch delete profanity words
[**ListProfanityWords**](ModerationAPI.md#ListProfanityWords) | **Post** /v4/profanity-word/list | List profanity words
[**RemoveProfanityWord**](ModerationAPI.md#RemoveProfanityWord) | **Post** /v4/profanity-word/remove | Delete profanity word



## BatchAddProfanityWords

> ProfanityWordBatchAddResponse BatchAddProfanityWords(ctx).ProfanityWordBatchAddRequest(profanityWordBatchAddRequest).Execute()

Batch add profanity words

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
	profanityWordBatchAddRequest := *openapiclient.NewProfanityWordBatchAddRequest([]openapiclient.ProfanityWordItem{*openapiclient.NewProfanityWordItem("Word_example")}) // ProfanityWordBatchAddRequest | 

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
	resp, r, err := apiClient.ModerationAPI.BatchAddProfanityWords(context.Background()).ProfanityWordBatchAddRequest(profanityWordBatchAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ModerationAPI.BatchAddProfanityWords``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchAddProfanityWords`: ProfanityWordBatchAddResponse
	fmt.Fprintf(os.Stdout, "Response from `ModerationAPI.BatchAddProfanityWords`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchAddProfanityWordsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profanityWordBatchAddRequest** | [**ProfanityWordBatchAddRequest**](ProfanityWordBatchAddRequest.md) |  | 

### Return type

[**ProfanityWordBatchAddResponse**](ProfanityWordBatchAddResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BatchRemoveProfanityWords

> CodeOnlyResponse BatchRemoveProfanityWords(ctx).ProfanityWordBatchDeleteRequest(profanityWordBatchDeleteRequest).Execute()

Batch delete profanity words

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
	profanityWordBatchDeleteRequest := *openapiclient.NewProfanityWordBatchDeleteRequest([]string{"Words_example"}) // ProfanityWordBatchDeleteRequest | 

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
	resp, r, err := apiClient.ModerationAPI.BatchRemoveProfanityWords(context.Background()).ProfanityWordBatchDeleteRequest(profanityWordBatchDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ModerationAPI.BatchRemoveProfanityWords``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchRemoveProfanityWords`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ModerationAPI.BatchRemoveProfanityWords`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchRemoveProfanityWordsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profanityWordBatchDeleteRequest** | [**ProfanityWordBatchDeleteRequest**](ProfanityWordBatchDeleteRequest.md) |  | 

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


## ListProfanityWords

> ProfanityWordListResponse ListProfanityWords(ctx).ProfanityWordListRequest(profanityWordListRequest).Execute()

List profanity words

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
	profanityWordListRequest := *openapiclient.NewProfanityWordListRequest() // ProfanityWordListRequest | 

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
	resp, r, err := apiClient.ModerationAPI.ListProfanityWords(context.Background()).ProfanityWordListRequest(profanityWordListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ModerationAPI.ListProfanityWords``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListProfanityWords`: ProfanityWordListResponse
	fmt.Fprintf(os.Stdout, "Response from `ModerationAPI.ListProfanityWords`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListProfanityWordsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profanityWordListRequest** | [**ProfanityWordListRequest**](ProfanityWordListRequest.md) |  | 

### Return type

[**ProfanityWordListResponse**](ProfanityWordListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveProfanityWord

> CodeOnlyResponse RemoveProfanityWord(ctx).ProfanityWordDeleteRequest(profanityWordDeleteRequest).Execute()

Delete profanity word

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
	profanityWordDeleteRequest := *openapiclient.NewProfanityWordDeleteRequest("Word_example") // ProfanityWordDeleteRequest | 

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
	resp, r, err := apiClient.ModerationAPI.RemoveProfanityWord(context.Background()).ProfanityWordDeleteRequest(profanityWordDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ModerationAPI.RemoveProfanityWord``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveProfanityWord`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ModerationAPI.RemoveProfanityWord`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveProfanityWordRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profanityWordDeleteRequest** | [**ProfanityWordDeleteRequest**](ProfanityWordDeleteRequest.md) |  | 

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


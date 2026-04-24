# UserBlocklistAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddUserBlocklist**](UserBlocklistAPI.md#AddUserBlocklist) | **Post** /v4/user/blocklist/add | Add to blocklist
[**GetUserBlocklist**](UserBlocklistAPI.md#GetUserBlocklist) | **Post** /v4/user/blocklist/get | Get blocklist
[**RemoveUserBlocklist**](UserBlocklistAPI.md#RemoveUserBlocklist) | **Post** /v4/user/blocklist/remove | Remove from blocklist



## AddUserBlocklist

> CodeOnlyResponse AddUserBlocklist(ctx).UserBlocklistAddRequest(userBlocklistAddRequest).Execute()

Add to blocklist



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
	userBlocklistAddRequest := *openapiclient.NewUserBlocklistAddRequest("UserId_example", []string{"TargetUserIds_example"}) // UserBlocklistAddRequest | 

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
	resp, r, err := apiClient.UserBlocklistAPI.AddUserBlocklist(context.Background()).UserBlocklistAddRequest(userBlocklistAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserBlocklistAPI.AddUserBlocklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddUserBlocklist`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserBlocklistAPI.AddUserBlocklist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddUserBlocklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userBlocklistAddRequest** | [**UserBlocklistAddRequest**](UserBlocklistAddRequest.md) |  | 

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


## GetUserBlocklist

> UserBlocklistGetResponse GetUserBlocklist(ctx).UserBlocklistGetRequest(userBlocklistGetRequest).Execute()

Get blocklist



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
	userBlocklistGetRequest := *openapiclient.NewUserBlocklistGetRequest("UserId_example") // UserBlocklistGetRequest | 

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
	resp, r, err := apiClient.UserBlocklistAPI.GetUserBlocklist(context.Background()).UserBlocklistGetRequest(userBlocklistGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserBlocklistAPI.GetUserBlocklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserBlocklist`: UserBlocklistGetResponse
	fmt.Fprintf(os.Stdout, "Response from `UserBlocklistAPI.GetUserBlocklist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetUserBlocklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userBlocklistGetRequest** | [**UserBlocklistGetRequest**](UserBlocklistGetRequest.md) |  | 

### Return type

[**UserBlocklistGetResponse**](UserBlocklistGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveUserBlocklist

> CodeOnlyResponse RemoveUserBlocklist(ctx).UserBlocklistRemoveRequest(userBlocklistRemoveRequest).Execute()

Remove from blocklist



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
	userBlocklistRemoveRequest := *openapiclient.NewUserBlocklistRemoveRequest("UserId_example", []string{"BlockedUserIds_example"}) // UserBlocklistRemoveRequest | 

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
	resp, r, err := apiClient.UserBlocklistAPI.RemoveUserBlocklist(context.Background()).UserBlocklistRemoveRequest(userBlocklistRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserBlocklistAPI.RemoveUserBlocklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveUserBlocklist`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserBlocklistAPI.RemoveUserBlocklist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveUserBlocklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userBlocklistRemoveRequest** | [**UserBlocklistRemoveRequest**](UserBlocklistRemoveRequest.md) |  | 

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


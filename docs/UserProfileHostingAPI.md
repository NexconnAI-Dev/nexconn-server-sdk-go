# UserProfileHostingAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BatchGetUserProfiles**](UserProfileHostingAPI.md#BatchGetUserProfiles) | **Post** /v4/user/profile/batch/get | Batch get user profiles
[**DeleteUserProfiles**](UserProfileHostingAPI.md#DeleteUserProfiles) | **Post** /v4/user/profile/delete | Clear user profiles
[**ListUserProfiles**](UserProfileHostingAPI.md#ListUserProfiles) | **Post** /v4/user/profile/list | List user profiles
[**SetUserProfile**](UserProfileHostingAPI.md#SetUserProfile) | **Post** /v4/user/profile/set | Set user profile



## BatchGetUserProfiles

> UserProfileBatchGetResponse BatchGetUserProfiles(ctx).UserIdsMax20Request(userIdsMax20Request).Execute()

Batch get user profiles

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
	userIdsMax20Request := *openapiclient.NewUserIdsMax20Request([]string{"UserIds_example"}) // UserIdsMax20Request | 

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
	resp, r, err := apiClient.UserProfileHostingAPI.BatchGetUserProfiles(context.Background()).UserIdsMax20Request(userIdsMax20Request).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserProfileHostingAPI.BatchGetUserProfiles``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchGetUserProfiles`: UserProfileBatchGetResponse
	fmt.Fprintf(os.Stdout, "Response from `UserProfileHostingAPI.BatchGetUserProfiles`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchGetUserProfilesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userIdsMax20Request** | [**UserIdsMax20Request**](UserIdsMax20Request.md) |  | 

### Return type

[**UserProfileBatchGetResponse**](UserProfileBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteUserProfiles

> CodeOnlyResponse DeleteUserProfiles(ctx).UserIdsMax20Request(userIdsMax20Request).Execute()

Clear user profiles

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
	userIdsMax20Request := *openapiclient.NewUserIdsMax20Request([]string{"UserIds_example"}) // UserIdsMax20Request | 

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
	resp, r, err := apiClient.UserProfileHostingAPI.DeleteUserProfiles(context.Background()).UserIdsMax20Request(userIdsMax20Request).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserProfileHostingAPI.DeleteUserProfiles``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteUserProfiles`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserProfileHostingAPI.DeleteUserProfiles`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteUserProfilesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userIdsMax20Request** | [**UserIdsMax20Request**](UserIdsMax20Request.md) |  | 

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


## ListUserProfiles

> UserProfileListResponse ListUserProfiles(ctx).UserProfileListRequest(userProfileListRequest).Execute()

List user profiles

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
	userProfileListRequest := *openapiclient.NewUserProfileListRequest() // UserProfileListRequest | 

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
	resp, r, err := apiClient.UserProfileHostingAPI.ListUserProfiles(context.Background()).UserProfileListRequest(userProfileListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserProfileHostingAPI.ListUserProfiles``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListUserProfiles`: UserProfileListResponse
	fmt.Fprintf(os.Stdout, "Response from `UserProfileHostingAPI.ListUserProfiles`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListUserProfilesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userProfileListRequest** | [**UserProfileListRequest**](UserProfileListRequest.md) |  | 

### Return type

[**UserProfileListResponse**](UserProfileListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SetUserProfile

> UserProfileSetResponse SetUserProfile(ctx).UserProfileSetRequest(userProfileSetRequest).Execute()

Set user profile

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
	userProfileSetRequest := *openapiclient.NewUserProfileSetRequest("UserId_example") // UserProfileSetRequest | 

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
	resp, r, err := apiClient.UserProfileHostingAPI.SetUserProfile(context.Background()).UserProfileSetRequest(userProfileSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserProfileHostingAPI.SetUserProfile``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetUserProfile`: UserProfileSetResponse
	fmt.Fprintf(os.Stdout, "Response from `UserProfileHostingAPI.SetUserProfile`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetUserProfileRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userProfileSetRequest** | [**UserProfileSetRequest**](UserProfileSetRequest.md) |  | 

### Return type

[**UserProfileSetResponse**](UserProfileSetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


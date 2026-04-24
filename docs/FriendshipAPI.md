# FriendshipAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddFriend**](FriendshipAPI.md#AddFriend) | **Post** /v4/friend/add | Add friend
[**GetFriendPermission**](FriendshipAPI.md#GetFriendPermission) | **Post** /v4/friend/permission/get | Get friend permission
[**GetFriendRelationships**](FriendshipAPI.md#GetFriendRelationships) | **Post** /v4/friend/relationship/get | Get friend relationships
[**ListFriends**](FriendshipAPI.md#ListFriends) | **Post** /v4/friend/list | List friends
[**RemoveAllFriends**](FriendshipAPI.md#RemoveAllFriends) | **Post** /v4/friend/remove-all | Clean all friends
[**RemoveFriends**](FriendshipAPI.md#RemoveFriends) | **Post** /v4/friend/remove | Delete friends
[**SetFriendPermission**](FriendshipAPI.md#SetFriendPermission) | **Post** /v4/friend/permission/set | Set friend permission
[**SetFriendProfile**](FriendshipAPI.md#SetFriendProfile) | **Post** /v4/friend/profile/set | Set friend profile



## AddFriend

> CodeOnlyResponse AddFriend(ctx).FriendAddRequest(friendAddRequest).Execute()

Add friend

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
	friendAddRequest := *openapiclient.NewFriendAddRequest("UserId_example", "TargetId_example") // FriendAddRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.AddFriend(context.Background()).FriendAddRequest(friendAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.AddFriend``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddFriend`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.AddFriend`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddFriendRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendAddRequest** | [**FriendAddRequest**](FriendAddRequest.md) |  | 

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


## GetFriendPermission

> FriendPermissionGetResponse GetFriendPermission(ctx).FriendPermissionGetRequest(friendPermissionGetRequest).Execute()

Get friend permission

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
	friendPermissionGetRequest := *openapiclient.NewFriendPermissionGetRequest([]string{"UserIds_example"}) // FriendPermissionGetRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.GetFriendPermission(context.Background()).FriendPermissionGetRequest(friendPermissionGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.GetFriendPermission``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetFriendPermission`: FriendPermissionGetResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.GetFriendPermission`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetFriendPermissionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendPermissionGetRequest** | [**FriendPermissionGetRequest**](FriendPermissionGetRequest.md) |  | 

### Return type

[**FriendPermissionGetResponse**](FriendPermissionGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetFriendRelationships

> FriendRelationshipGetResponse GetFriendRelationships(ctx).FriendRelationshipGetRequest(friendRelationshipGetRequest).Execute()

Get friend relationships

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
	friendRelationshipGetRequest := *openapiclient.NewFriendRelationshipGetRequest("UserId_example", []string{"TargetIds_example"}) // FriendRelationshipGetRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.GetFriendRelationships(context.Background()).FriendRelationshipGetRequest(friendRelationshipGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.GetFriendRelationships``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetFriendRelationships`: FriendRelationshipGetResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.GetFriendRelationships`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetFriendRelationshipsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendRelationshipGetRequest** | [**FriendRelationshipGetRequest**](FriendRelationshipGetRequest.md) |  | 

### Return type

[**FriendRelationshipGetResponse**](FriendRelationshipGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListFriends

> FriendListResponse ListFriends(ctx).FriendListRequest(friendListRequest).Execute()

List friends

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
	friendListRequest := *openapiclient.NewFriendListRequest("UserId_example") // FriendListRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.ListFriends(context.Background()).FriendListRequest(friendListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.ListFriends``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListFriends`: FriendListResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.ListFriends`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListFriendsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendListRequest** | [**FriendListRequest**](FriendListRequest.md) |  | 

### Return type

[**FriendListResponse**](FriendListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveAllFriends

> CodeOnlyResponse RemoveAllFriends(ctx).FriendCleanRequest(friendCleanRequest).Execute()

Clean all friends

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
	friendCleanRequest := *openapiclient.NewFriendCleanRequest("UserId_example") // FriendCleanRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.RemoveAllFriends(context.Background()).FriendCleanRequest(friendCleanRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.RemoveAllFriends``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveAllFriends`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.RemoveAllFriends`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveAllFriendsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendCleanRequest** | [**FriendCleanRequest**](FriendCleanRequest.md) |  | 

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


## RemoveFriends

> CodeOnlyResponse RemoveFriends(ctx).FriendDeleteRequest(friendDeleteRequest).Execute()

Delete friends

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
	friendDeleteRequest := *openapiclient.NewFriendDeleteRequest("UserId_example", []string{"TargetIds_example"}) // FriendDeleteRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.RemoveFriends(context.Background()).FriendDeleteRequest(friendDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.RemoveFriends``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveFriends`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.RemoveFriends`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveFriendsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendDeleteRequest** | [**FriendDeleteRequest**](FriendDeleteRequest.md) |  | 

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


## SetFriendPermission

> CodeOnlyResponse SetFriendPermission(ctx).FriendPermissionSetRequest(friendPermissionSetRequest).Execute()

Set friend permission

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
	friendPermissionSetRequest := *openapiclient.NewFriendPermissionSetRequest([]string{"UserIds_example"}, int32(123)) // FriendPermissionSetRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.SetFriendPermission(context.Background()).FriendPermissionSetRequest(friendPermissionSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.SetFriendPermission``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetFriendPermission`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.SetFriendPermission`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetFriendPermissionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendPermissionSetRequest** | [**FriendPermissionSetRequest**](FriendPermissionSetRequest.md) |  | 

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


## SetFriendProfile

> CodeOnlyResponse SetFriendProfile(ctx).FriendProfileSetRequest(friendProfileSetRequest).Execute()

Set friend profile

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
	friendProfileSetRequest := *openapiclient.NewFriendProfileSetRequest("UserId_example", "TargetId_example") // FriendProfileSetRequest | 

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
	resp, r, err := apiClient.FriendshipAPI.SetFriendProfile(context.Background()).FriendProfileSetRequest(friendProfileSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `FriendshipAPI.SetFriendProfile``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetFriendProfile`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `FriendshipAPI.SetFriendProfile`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetFriendProfileRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **friendProfileSetRequest** | [**FriendProfileSetRequest**](FriendProfileSetRequest.md) |  | 

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


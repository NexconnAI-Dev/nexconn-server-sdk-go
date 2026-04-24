# UserManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BanUsers**](UserManagementAPI.md#BanUsers) | **Post** /v4/user/ban | Ban a user
[**BatchGetUserTags**](UserManagementAPI.md#BatchGetUserTags) | **Post** /v4/user/tag/batch/get | Get user tags
[**BatchSetUserTags**](UserManagementAPI.md#BatchSetUserTags) | **Post** /v4/user/tag/batch/set | Batch set user tags
[**ExpireAccessToken**](UserManagementAPI.md#ExpireAccessToken) | **Post** /v4/auth/access-token/expire | Expire an access token
[**GetUser**](UserManagementAPI.md#GetUser) | **Post** /v4/user/get | Get user info
[**GetUserConnectionStatus**](UserManagementAPI.md#GetUserConnectionStatus) | **Post** /v4/user/connection-status/get | Check user online status
[**IssueAccessToken**](UserManagementAPI.md#IssueAccessToken) | **Post** /v4/auth/access-token/issue | Register a user
[**ListBannedUsers**](UserManagementAPI.md#ListBannedUsers) | **Post** /v4/user/ban/list | List banned users
[**ListChannelTypeMute**](UserManagementAPI.md#ListChannelTypeMute) | **Post** /v4/channel-type/mute/list | List muted direct channel users
[**ListSoftDeletedUsers**](UserManagementAPI.md#ListSoftDeletedUsers) | **Post** /v4/user/soft-deleted/list | Query soft-deleted users
[**RestoreUsers**](UserManagementAPI.md#RestoreUsers) | **Post** /v4/user/restore | Restore a user
[**SetChannelTypeMute**](UserManagementAPI.md#SetChannelTypeMute) | **Post** /v4/channel-type/mute/set | Mute a user in direct channels
[**SoftDeleteUsers**](UserManagementAPI.md#SoftDeleteUsers) | **Post** /v4/user/soft-delete | Soft-delete a user
[**UnbanUsers**](UserManagementAPI.md#UnbanUsers) | **Post** /v4/user/unban | Unban a user
[**UpdateUser**](UserManagementAPI.md#UpdateUser) | **Post** /v4/user/update | Update user info



## BanUsers

> CodeOnlyResponse BanUsers(ctx).UserBanRequest(userBanRequest).Execute()

Ban a user



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
	userBanRequest := *openapiclient.NewUserBanRequest([]string{"UserIds_example"}, int32(123)) // UserBanRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.BanUsers(context.Background()).UserBanRequest(userBanRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.BanUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BanUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.BanUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBanUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userBanRequest** | [**UserBanRequest**](UserBanRequest.md) |  | 

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


## BatchGetUserTags

> UserTagBatchGetResponse BatchGetUserTags(ctx).UserTagBatchGetRequest(userTagBatchGetRequest).Execute()

Get user tags



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
	userTagBatchGetRequest := *openapiclient.NewUserTagBatchGetRequest([]string{"UserIds_example"}) // UserTagBatchGetRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.BatchGetUserTags(context.Background()).UserTagBatchGetRequest(userTagBatchGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.BatchGetUserTags``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchGetUserTags`: UserTagBatchGetResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.BatchGetUserTags`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchGetUserTagsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userTagBatchGetRequest** | [**UserTagBatchGetRequest**](UserTagBatchGetRequest.md) |  | 

### Return type

[**UserTagBatchGetResponse**](UserTagBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BatchSetUserTags

> CodeOnlyResponse BatchSetUserTags(ctx).UserTagBatchSetRequest(userTagBatchSetRequest).Execute()

Batch set user tags



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
	userTagBatchSetRequest := *openapiclient.NewUserTagBatchSetRequest([]string{"UserIds_example"}, []string{"Tags_example"}) // UserTagBatchSetRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.BatchSetUserTags(context.Background()).UserTagBatchSetRequest(userTagBatchSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.BatchSetUserTags``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BatchSetUserTags`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.BatchSetUserTags`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBatchSetUserTagsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userTagBatchSetRequest** | [**UserTagBatchSetRequest**](UserTagBatchSetRequest.md) |  | 

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


## ExpireAccessToken

> CodeOnlyResponse ExpireAccessToken(ctx).AccessTokenExpireRequest(accessTokenExpireRequest).Execute()

Expire an access token



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
	accessTokenExpireRequest := *openapiclient.NewAccessTokenExpireRequest([]string{"UserIds_example"}, int64(123)) // AccessTokenExpireRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.ExpireAccessToken(context.Background()).AccessTokenExpireRequest(accessTokenExpireRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.ExpireAccessToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ExpireAccessToken`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.ExpireAccessToken`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiExpireAccessTokenRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accessTokenExpireRequest** | [**AccessTokenExpireRequest**](AccessTokenExpireRequest.md) |  | 

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


## GetUser

> UserGetResponse GetUser(ctx).UserGetRequest(userGetRequest).Execute()

Get user info



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
	userGetRequest := *openapiclient.NewUserGetRequest("UserId_example") // UserGetRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.GetUser(context.Background()).UserGetRequest(userGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.GetUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUser`: UserGetResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.GetUser`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userGetRequest** | [**UserGetRequest**](UserGetRequest.md) |  | 

### Return type

[**UserGetResponse**](UserGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserConnectionStatus

> UserConnectionStatusResponse GetUserConnectionStatus(ctx).UserConnectionStatusRequest(userConnectionStatusRequest).Execute()

Check user online status



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
	userConnectionStatusRequest := *openapiclient.NewUserConnectionStatusRequest("UserId_example") // UserConnectionStatusRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.GetUserConnectionStatus(context.Background()).UserConnectionStatusRequest(userConnectionStatusRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.GetUserConnectionStatus``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserConnectionStatus`: UserConnectionStatusResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.GetUserConnectionStatus`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetUserConnectionStatusRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userConnectionStatusRequest** | [**UserConnectionStatusRequest**](UserConnectionStatusRequest.md) |  | 

### Return type

[**UserConnectionStatusResponse**](UserConnectionStatusResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## IssueAccessToken

> AccessTokenIssueResponse IssueAccessToken(ctx).AccessTokenIssueRequest(accessTokenIssueRequest).Execute()

Register a user



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
	accessTokenIssueRequest := *openapiclient.NewAccessTokenIssueRequest("UserId_example", "Name_example") // AccessTokenIssueRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.IssueAccessToken(context.Background()).AccessTokenIssueRequest(accessTokenIssueRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.IssueAccessToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `IssueAccessToken`: AccessTokenIssueResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.IssueAccessToken`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiIssueAccessTokenRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accessTokenIssueRequest** | [**AccessTokenIssueRequest**](AccessTokenIssueRequest.md) |  | 

### Return type

[**AccessTokenIssueResponse**](AccessTokenIssueResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBannedUsers

> UserBanListResponse ListBannedUsers(ctx).UserBanListRequest(userBanListRequest).Execute()

List banned users



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
	userBanListRequest := *openapiclient.NewUserBanListRequest() // UserBanListRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.ListBannedUsers(context.Background()).UserBanListRequest(userBanListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.ListBannedUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBannedUsers`: UserBanListResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.ListBannedUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListBannedUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userBanListRequest** | [**UserBanListRequest**](UserBanListRequest.md) |  | 

### Return type

[**UserBanListResponse**](UserBanListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListChannelTypeMute

> ChannelTypeMuteListResponse ListChannelTypeMute(ctx).ChannelTypeMuteListRequest(channelTypeMuteListRequest).Execute()

List muted direct channel users



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
	channelTypeMuteListRequest := *openapiclient.NewChannelTypeMuteListRequest("ChannelType_example") // ChannelTypeMuteListRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.ListChannelTypeMute(context.Background()).ChannelTypeMuteListRequest(channelTypeMuteListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.ListChannelTypeMute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListChannelTypeMute`: ChannelTypeMuteListResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.ListChannelTypeMute`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListChannelTypeMuteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeMuteListRequest** | [**ChannelTypeMuteListRequest**](ChannelTypeMuteListRequest.md) |  | 

### Return type

[**ChannelTypeMuteListResponse**](ChannelTypeMuteListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListSoftDeletedUsers

> UserSoftDeletedListResponse ListSoftDeletedUsers(ctx).UserSoftDeletedListRequest(userSoftDeletedListRequest).Execute()

Query soft-deleted users



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
	userSoftDeletedListRequest := *openapiclient.NewUserSoftDeletedListRequest() // UserSoftDeletedListRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.ListSoftDeletedUsers(context.Background()).UserSoftDeletedListRequest(userSoftDeletedListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.ListSoftDeletedUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListSoftDeletedUsers`: UserSoftDeletedListResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.ListSoftDeletedUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListSoftDeletedUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userSoftDeletedListRequest** | [**UserSoftDeletedListRequest**](UserSoftDeletedListRequest.md) |  | 

### Return type

[**UserSoftDeletedListResponse**](UserSoftDeletedListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RestoreUsers

> UserOperationResponse RestoreUsers(ctx).UserIdsMax100Request(userIdsMax100Request).Execute()

Restore a user



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
	userIdsMax100Request := *openapiclient.NewUserIdsMax100Request([]string{"UserIds_example"}) // UserIdsMax100Request | 

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
	resp, r, err := apiClient.UserManagementAPI.RestoreUsers(context.Background()).UserIdsMax100Request(userIdsMax100Request).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.RestoreUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RestoreUsers`: UserOperationResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.RestoreUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRestoreUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userIdsMax100Request** | [**UserIdsMax100Request**](UserIdsMax100Request.md) |  | 

### Return type

[**UserOperationResponse**](UserOperationResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SetChannelTypeMute

> CodeOnlyResponse SetChannelTypeMute(ctx).ChannelTypeMuteSetRequest(channelTypeMuteSetRequest).Execute()

Mute a user in direct channels



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
	channelTypeMuteSetRequest := *openapiclient.NewChannelTypeMuteSetRequest([]string{"UserIds_example"}, int32(123), []string{"ChannelTypes_example"}) // ChannelTypeMuteSetRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.SetChannelTypeMute(context.Background()).ChannelTypeMuteSetRequest(channelTypeMuteSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.SetChannelTypeMute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetChannelTypeMute`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.SetChannelTypeMute`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetChannelTypeMuteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeMuteSetRequest** | [**ChannelTypeMuteSetRequest**](ChannelTypeMuteSetRequest.md) |  | 

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


## SoftDeleteUsers

> UserOperationResponse SoftDeleteUsers(ctx).UserIdsMax100Request(userIdsMax100Request).Execute()

Soft-delete a user



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
	userIdsMax100Request := *openapiclient.NewUserIdsMax100Request([]string{"UserIds_example"}) // UserIdsMax100Request | 

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
	resp, r, err := apiClient.UserManagementAPI.SoftDeleteUsers(context.Background()).UserIdsMax100Request(userIdsMax100Request).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.SoftDeleteUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SoftDeleteUsers`: UserOperationResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.SoftDeleteUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSoftDeleteUsersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userIdsMax100Request** | [**UserIdsMax100Request**](UserIdsMax100Request.md) |  | 

### Return type

[**UserOperationResponse**](UserOperationResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UnbanUsers

> CodeOnlyResponse UnbanUsers(ctx).UserIdsMax20Request(userIdsMax20Request).Execute()

Unban a user



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
	resp, r, err := apiClient.UserManagementAPI.UnbanUsers(context.Background()).UserIdsMax20Request(userIdsMax20Request).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.UnbanUsers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UnbanUsers`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.UnbanUsers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUnbanUsersRequest struct via the builder pattern


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


## UpdateUser

> CodeOnlyResponse UpdateUser(ctx).UserUpdateRequest(userUpdateRequest).Execute()

Update user info



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
	userUpdateRequest := *openapiclient.NewUserUpdateRequest("UserId_example") // UserUpdateRequest | 

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
	resp, r, err := apiClient.UserManagementAPI.UpdateUser(context.Background()).UserUpdateRequest(userUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UserManagementAPI.UpdateUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateUser`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `UserManagementAPI.UpdateUser`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userUpdateRequest** | [**UserUpdateRequest**](UserUpdateRequest.md) |  | 

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


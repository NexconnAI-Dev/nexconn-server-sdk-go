# SystemMessagesAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BroadcastMessageOnline**](SystemMessagesAPI.md#BroadcastMessageOnline) | **Post** /v4/system-channel/message/broadcast-online | Broadcast to online users
[**BroadcastSystemChannelMessage**](SystemMessagesAPI.md#BroadcastSystemChannelMessage) | **Post** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent)
[**DeleteBroadcastMessage**](SystemMessagesAPI.md#DeleteBroadcastMessage) | **Post** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users
[**SendSystemChannelMessage**](SystemMessagesAPI.md#SendSystemChannelMessage) | **Post** /v4/system-channel/message/send | Send a system message
[**SendSystemChannelPushByPackage**](SystemMessagesAPI.md#SendSystemChannelPushByPackage) | **Post** /v4/system-channel/app-package-users/send | Push by app package name
[**SendSystemChannelPushByTag**](SystemMessagesAPI.md#SendSystemChannelPushByTag) | **Post** /v4/system-channel/tagged-users/send | Push to tagged users



## BroadcastMessageOnline

> SingleMessageIdResponse BroadcastMessageOnline(ctx).SystemChannelBroadcastOnlineRequest(systemChannelBroadcastOnlineRequest).Execute()

Broadcast to online users



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
	systemChannelBroadcastOnlineRequest := *openapiclient.NewSystemChannelBroadcastOnlineRequest("FromUserId_example", "MessageType_example", "Content_example") // SystemChannelBroadcastOnlineRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.BroadcastMessageOnline(context.Background()).SystemChannelBroadcastOnlineRequest(systemChannelBroadcastOnlineRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.BroadcastMessageOnline``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BroadcastMessageOnline`: SingleMessageIdResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.BroadcastMessageOnline`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBroadcastMessageOnlineRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelBroadcastOnlineRequest** | [**SystemChannelBroadcastOnlineRequest**](SystemChannelBroadcastOnlineRequest.md) |  | 

### Return type

[**SingleMessageIdResponse**](SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BroadcastSystemChannelMessage

> SingleMessageIdResponse BroadcastSystemChannelMessage(ctx).SystemChannelBroadcastAllRequest(systemChannelBroadcastAllRequest).Execute()

Broadcast to all users (persistent)



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
	systemChannelBroadcastAllRequest := *openapiclient.NewSystemChannelBroadcastAllRequest("FromUserId_example", "MessageType_example", "Content_example") // SystemChannelBroadcastAllRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.BroadcastSystemChannelMessage(context.Background()).SystemChannelBroadcastAllRequest(systemChannelBroadcastAllRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.BroadcastSystemChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BroadcastSystemChannelMessage`: SingleMessageIdResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.BroadcastSystemChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBroadcastSystemChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelBroadcastAllRequest** | [**SystemChannelBroadcastAllRequest**](SystemChannelBroadcastAllRequest.md) |  | 

### Return type

[**SingleMessageIdResponse**](SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteBroadcastMessage

> CodeOnlyResponse DeleteBroadcastMessage(ctx).SystemChannelBroadcastDeleteRequest(systemChannelBroadcastDeleteRequest).Execute()

Recall broadcast to all users



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
	systemChannelBroadcastDeleteRequest := *openapiclient.NewSystemChannelBroadcastDeleteRequest("FromUserId_example", "MessageId_example") // SystemChannelBroadcastDeleteRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.DeleteBroadcastMessage(context.Background()).SystemChannelBroadcastDeleteRequest(systemChannelBroadcastDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.DeleteBroadcastMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteBroadcastMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.DeleteBroadcastMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteBroadcastMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelBroadcastDeleteRequest** | [**SystemChannelBroadcastDeleteRequest**](SystemChannelBroadcastDeleteRequest.md) |  | 

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


## SendSystemChannelMessage

> UserMessageSendResponse SendSystemChannelMessage(ctx).SystemChannelMessageSendRequest(systemChannelMessageSendRequest).Execute()

Send a system message



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
	systemChannelMessageSendRequest := *openapiclient.NewSystemChannelMessageSendRequest("FromUserId_example", []string{"ToUserIds_example"}, "MessageType_example", "Content_example") // SystemChannelMessageSendRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.SendSystemChannelMessage(context.Background()).SystemChannelMessageSendRequest(systemChannelMessageSendRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.SendSystemChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendSystemChannelMessage`: UserMessageSendResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.SendSystemChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendSystemChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelMessageSendRequest** | [**SystemChannelMessageSendRequest**](SystemChannelMessageSendRequest.md) |  | 

### Return type

[**UserMessageSendResponse**](UserMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SendSystemChannelPushByPackage

> SystemChannelPushResponse SendSystemChannelPushByPackage(ctx).SystemChannelPushRequest(systemChannelPushRequest).Execute()

Push by app package name



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
	systemChannelPushRequest := *openapiclient.NewSystemChannelPushRequest([]string{"Platform_example"}, "FromUserId_example", *openapiclient.NewSystemChannelPushAudience(), *openapiclient.NewSystemChannelPushMessage("Content_example", "MessageType_example"), *openapiclient.NewSystemChannelPushNotification()) // SystemChannelPushRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.SendSystemChannelPushByPackage(context.Background()).SystemChannelPushRequest(systemChannelPushRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.SendSystemChannelPushByPackage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendSystemChannelPushByPackage`: SystemChannelPushResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.SendSystemChannelPushByPackage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendSystemChannelPushByPackageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelPushRequest** | [**SystemChannelPushRequest**](SystemChannelPushRequest.md) |  | 

### Return type

[**SystemChannelPushResponse**](SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SendSystemChannelPushByTag

> SystemChannelPushResponse SendSystemChannelPushByTag(ctx).SystemChannelPushRequest(systemChannelPushRequest).Execute()

Push to tagged users



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
	systemChannelPushRequest := *openapiclient.NewSystemChannelPushRequest([]string{"Platform_example"}, "FromUserId_example", *openapiclient.NewSystemChannelPushAudience(), *openapiclient.NewSystemChannelPushMessage("Content_example", "MessageType_example"), *openapiclient.NewSystemChannelPushNotification()) // SystemChannelPushRequest | 

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
	resp, r, err := apiClient.SystemMessagesAPI.SendSystemChannelPushByTag(context.Background()).SystemChannelPushRequest(systemChannelPushRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SystemMessagesAPI.SendSystemChannelPushByTag``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendSystemChannelPushByTag`: SystemChannelPushResponse
	fmt.Fprintf(os.Stdout, "Response from `SystemMessagesAPI.SendSystemChannelPushByTag`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendSystemChannelPushByTagRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **systemChannelPushRequest** | [**SystemChannelPushRequest**](SystemChannelPushRequest.md) |  | 

### Return type

[**SystemChannelPushResponse**](SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


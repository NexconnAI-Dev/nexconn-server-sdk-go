# ChannelManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddTagToChannels**](ChannelManagementAPI.md#AddTagToChannels) | **Post** /v4/channel/tag/add | Add tag to channel
[**AddUserChannelTags**](ChannelManagementAPI.md#AddUserChannelTags) | **Post** /v4/user/channel/tag/add | Add user channel tag
[**GetChannelAttribute**](ChannelManagementAPI.md#GetChannelAttribute) | **Post** /v4/channel/attribute/get | Get channel attributes
[**GetChannelPushNotification**](ChannelManagementAPI.md#GetChannelPushNotification) | **Post** /v4/channel/push/get | Get channel DND
[**GetChannelTypeNotification**](ChannelManagementAPI.md#GetChannelTypeNotification) | **Post** /v4/channel-type/push/get | Get DND by channel type
[**ListChannelsByTag**](ChannelManagementAPI.md#ListChannelsByTag) | **Post** /v4/channel/tag/list | Get channels by tag
[**ListUserChannelTags**](ChannelManagementAPI.md#ListUserChannelTags) | **Post** /v4/user/channel/tag/list | List user channel tags
[**RemoveTagFromChannels**](ChannelManagementAPI.md#RemoveTagFromChannels) | **Post** /v4/channel/tag/delete | Remove tag from channel
[**RemoveUserChannelTags**](ChannelManagementAPI.md#RemoveUserChannelTags) | **Post** /v4/user/channel/tag/remove | Remove user channel tag
[**SetChannelPin**](ChannelManagementAPI.md#SetChannelPin) | **Post** /v4/channel/pin/set | Pin a channel
[**SetChannelPushNotification**](ChannelManagementAPI.md#SetChannelPushNotification) | **Post** /v4/channel/push/set | Set channel DND
[**SetChannelTypeNotification**](ChannelManagementAPI.md#SetChannelTypeNotification) | **Post** /v4/channel-type/push/set | Set DND by channel type



## AddTagToChannels

> CodeOnlyResponse AddTagToChannels(ctx).ChannelTagAddRequest(channelTagAddRequest).Execute()

Add tag to channel



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
	channelTagAddRequest := *openapiclient.NewChannelTagAddRequest("UserId_example", "TagId_example", []openapiclient.ChannelTagTargetItem{*openapiclient.NewChannelTagTargetItem("ChannelId_example", int32(123))}) // ChannelTagAddRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.AddTagToChannels(context.Background()).ChannelTagAddRequest(channelTagAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.AddTagToChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddTagToChannels`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.AddTagToChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddTagToChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTagAddRequest** | [**ChannelTagAddRequest**](ChannelTagAddRequest.md) |  | 

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


## AddUserChannelTags

> CodeOnlyResponse AddUserChannelTags(ctx).UserChannelTagAddRequest(userChannelTagAddRequest).Execute()

Add user channel tag



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
	userChannelTagAddRequest := *openapiclient.NewUserChannelTagAddRequest("UserId_example", []openapiclient.UserChannelTagItem{*openapiclient.NewUserChannelTagItem("TagId_example", "TagName_example")}) // UserChannelTagAddRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.AddUserChannelTags(context.Background()).UserChannelTagAddRequest(userChannelTagAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.AddUserChannelTags``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddUserChannelTags`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.AddUserChannelTags`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddUserChannelTagsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userChannelTagAddRequest** | [**UserChannelTagAddRequest**](UserChannelTagAddRequest.md) |  | 

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


## GetChannelAttribute

> ChannelAttributeGetResponse GetChannelAttribute(ctx).ChannelAttributeGetRequest(channelAttributeGetRequest).Execute()

Get channel attributes



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
	channelAttributeGetRequest := *openapiclient.NewChannelAttributeGetRequest("UserId_example", "ChannelId_example", int32(123)) // ChannelAttributeGetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.GetChannelAttribute(context.Background()).ChannelAttributeGetRequest(channelAttributeGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.GetChannelAttribute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetChannelAttribute`: ChannelAttributeGetResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.GetChannelAttribute`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetChannelAttributeRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelAttributeGetRequest** | [**ChannelAttributeGetRequest**](ChannelAttributeGetRequest.md) |  | 

### Return type

[**ChannelAttributeGetResponse**](ChannelAttributeGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetChannelPushNotification

> ChannelPushGetResponse GetChannelPushNotification(ctx).ChannelPushGetRequest(channelPushGetRequest).Execute()

Get channel DND



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
	channelPushGetRequest := *openapiclient.NewChannelPushGetRequest("ChannelType_example", "RequestId_example", "ChannelId_example") // ChannelPushGetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.GetChannelPushNotification(context.Background()).ChannelPushGetRequest(channelPushGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.GetChannelPushNotification``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetChannelPushNotification`: ChannelPushGetResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.GetChannelPushNotification`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetChannelPushNotificationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelPushGetRequest** | [**ChannelPushGetRequest**](ChannelPushGetRequest.md) |  | 

### Return type

[**ChannelPushGetResponse**](ChannelPushGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetChannelTypeNotification

> ChannelTypeNotificationGetResponse GetChannelTypeNotification(ctx).ChannelTypeNotificationGetRequest(channelTypeNotificationGetRequest).Execute()

Get DND by channel type



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
	channelTypeNotificationGetRequest := *openapiclient.NewChannelTypeNotificationGetRequest("ChannelType_example", "RequestId_example") // ChannelTypeNotificationGetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.GetChannelTypeNotification(context.Background()).ChannelTypeNotificationGetRequest(channelTypeNotificationGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.GetChannelTypeNotification``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetChannelTypeNotification`: ChannelTypeNotificationGetResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.GetChannelTypeNotification`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetChannelTypeNotificationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeNotificationGetRequest** | [**ChannelTypeNotificationGetRequest**](ChannelTypeNotificationGetRequest.md) |  | 

### Return type

[**ChannelTypeNotificationGetResponse**](ChannelTypeNotificationGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListChannelsByTag

> ChannelTagListResponse ListChannelsByTag(ctx).ChannelTagListRequest(channelTagListRequest).Execute()

Get channels by tag



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
	channelTagListRequest := *openapiclient.NewChannelTagListRequest("UserId_example", "TagId_example") // ChannelTagListRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.ListChannelsByTag(context.Background()).ChannelTagListRequest(channelTagListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.ListChannelsByTag``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListChannelsByTag`: ChannelTagListResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.ListChannelsByTag`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListChannelsByTagRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTagListRequest** | [**ChannelTagListRequest**](ChannelTagListRequest.md) |  | 

### Return type

[**ChannelTagListResponse**](ChannelTagListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListUserChannelTags

> UserChannelTagListResponse ListUserChannelTags(ctx).UserChannelTagListRequest(userChannelTagListRequest).Execute()

List user channel tags

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
	userChannelTagListRequest := *openapiclient.NewUserChannelTagListRequest("UserId_example") // UserChannelTagListRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.ListUserChannelTags(context.Background()).UserChannelTagListRequest(userChannelTagListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.ListUserChannelTags``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListUserChannelTags`: UserChannelTagListResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.ListUserChannelTags`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListUserChannelTagsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userChannelTagListRequest** | [**UserChannelTagListRequest**](UserChannelTagListRequest.md) |  | 

### Return type

[**UserChannelTagListResponse**](UserChannelTagListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveTagFromChannels

> CodeOnlyResponse RemoveTagFromChannels(ctx).ChannelTagRemoveRequest(channelTagRemoveRequest).Execute()

Remove tag from channel



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
	channelTagRemoveRequest := *openapiclient.NewChannelTagRemoveRequest("UserId_example", "TagId_example", []openapiclient.ChannelTagTargetItem{*openapiclient.NewChannelTagTargetItem("ChannelId_example", int32(123))}) // ChannelTagRemoveRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.RemoveTagFromChannels(context.Background()).ChannelTagRemoveRequest(channelTagRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.RemoveTagFromChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveTagFromChannels`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.RemoveTagFromChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveTagFromChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTagRemoveRequest** | [**ChannelTagRemoveRequest**](ChannelTagRemoveRequest.md) |  | 

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


## RemoveUserChannelTags

> CodeOnlyResponse RemoveUserChannelTags(ctx).UserChannelTagRemoveRequest(userChannelTagRemoveRequest).Execute()

Remove user channel tag



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
	userChannelTagRemoveRequest := *openapiclient.NewUserChannelTagRemoveRequest("UserId_example", []string{"TagIds_example"}) // UserChannelTagRemoveRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.RemoveUserChannelTags(context.Background()).UserChannelTagRemoveRequest(userChannelTagRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.RemoveUserChannelTags``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveUserChannelTags`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.RemoveUserChannelTags`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveUserChannelTagsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userChannelTagRemoveRequest** | [**UserChannelTagRemoveRequest**](UserChannelTagRemoveRequest.md) |  | 

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


## SetChannelPin

> CodeOnlyResponse SetChannelPin(ctx).ChannelPinSetRequest(channelPinSetRequest).Execute()

Pin a channel



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
	channelPinSetRequest := *openapiclient.NewChannelPinSetRequest("UserId_example", int32(123), "ChannelId_example", false) // ChannelPinSetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.SetChannelPin(context.Background()).ChannelPinSetRequest(channelPinSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.SetChannelPin``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetChannelPin`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.SetChannelPin`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetChannelPinRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelPinSetRequest** | [**ChannelPinSetRequest**](ChannelPinSetRequest.md) |  | 

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


## SetChannelPushNotification

> CodeOnlyResponse SetChannelPushNotification(ctx).ChannelPushSetRequest(channelPushSetRequest).Execute()

Set channel DND



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
	channelPushSetRequest := *openapiclient.NewChannelPushSetRequest("ChannelType_example", "RequestId_example", "ChannelId_example", int32(123)) // ChannelPushSetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.SetChannelPushNotification(context.Background()).ChannelPushSetRequest(channelPushSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.SetChannelPushNotification``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetChannelPushNotification`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.SetChannelPushNotification`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetChannelPushNotificationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelPushSetRequest** | [**ChannelPushSetRequest**](ChannelPushSetRequest.md) |  | 

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


## SetChannelTypeNotification

> CodeOnlyResponse SetChannelTypeNotification(ctx).ChannelTypeNotificationSetRequest(channelTypeNotificationSetRequest).Execute()

Set DND by channel type



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
	channelTypeNotificationSetRequest := *openapiclient.NewChannelTypeNotificationSetRequest("ChannelType_example", "RequestId_example", int32(123)) // ChannelTypeNotificationSetRequest | 

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
	resp, r, err := apiClient.ChannelManagementAPI.SetChannelTypeNotification(context.Background()).ChannelTypeNotificationSetRequest(channelTypeNotificationSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ChannelManagementAPI.SetChannelTypeNotification``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetChannelTypeNotification`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `ChannelManagementAPI.SetChannelTypeNotification`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetChannelTypeNotificationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeNotificationSetRequest** | [**ChannelTypeNotificationSetRequest**](ChannelTypeNotificationSetRequest.md) |  | 

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


# MessageManagementAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**BroadcastOpenChannelMessage**](MessageManagementAPI.md#BroadcastOpenChannelMessage) | **Post** /v4/open-channel/message/broadcast | Broadcast to all open channels
[**DeleteChannelMessageHistory**](MessageManagementAPI.md#DeleteChannelMessageHistory) | **Post** /v4/channel/message/history/delete | Delete server-side channel message history
[**DeleteChannelTypeMessageMetadata**](MessageManagementAPI.md#DeleteChannelTypeMessageMetadata) | **Post** /v4/channel-type/message/metadata/delete | Delete message metadata
[**DeleteCommunityChannelMessageMetadata**](MessageManagementAPI.md#DeleteCommunityChannelMessageMetadata) | **Post** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys
[**DeleteMessage**](MessageManagementAPI.md#DeleteMessage) | **Post** /v4/message/delete | Delete a message (recall)
[**ListChannelTypeMessageMetadata**](MessageManagementAPI.md#ListChannelTypeMessageMetadata) | **Post** /v4/channel-type/message/metadata/list | Get message metadata
[**ListCommunityChannelMessageMetadata**](MessageManagementAPI.md#ListCommunityChannelMessageMetadata) | **Post** /v4/community-channel/message/metadata/list | List community-channel message metadata
[**SendCommunityChannelMessage**](MessageManagementAPI.md#SendCommunityChannelMessage) | **Post** /v4/community-channel/message/send | Send a community channel message
[**SendDirectChannelMessage**](MessageManagementAPI.md#SendDirectChannelMessage) | **Post** /v4/direct-channel/message/send | Send a direct message
[**SendGroupChannelMessage**](MessageManagementAPI.md#SendGroupChannelMessage) | **Post** /v4/group-channel/message/send | Send a group message
[**SendOpenChannelMessage**](MessageManagementAPI.md#SendOpenChannelMessage) | **Post** /v4/open-channel/message/send | Send an open channel message
[**SetChannelTypeMessageMetadata**](MessageManagementAPI.md#SetChannelTypeMessageMetadata) | **Post** /v4/channel-type/message/metadata/set | Set message metadata
[**SetCommunityChannelMessageMetadata**](MessageManagementAPI.md#SetCommunityChannelMessageMetadata) | **Post** /v4/community-channel/message/metadata/set | Set community-channel message metadata
[**UpdateCommunityChannelMessage**](MessageManagementAPI.md#UpdateCommunityChannelMessage) | **Post** /v4/community-channel/message/update | Update community-channel message
[**UpdateDirectChannelMessage**](MessageManagementAPI.md#UpdateDirectChannelMessage) | **Post** /v4/direct-channel/message/update | Update direct-channel message
[**UpdateGroupChannelMessage**](MessageManagementAPI.md#UpdateGroupChannelMessage) | **Post** /v4/group-channel/message/update | Update group-channel message



## BroadcastOpenChannelMessage

> CodeOnlyResponse BroadcastOpenChannelMessage(ctx).OpenChannelBroadcastRequest(openChannelBroadcastRequest).Execute()

Broadcast to all open channels



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
	openChannelBroadcastRequest := *openapiclient.NewOpenChannelBroadcastRequest("FromUserId_example", "MessageType_example", "Content_example") // OpenChannelBroadcastRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.BroadcastOpenChannelMessage(context.Background()).OpenChannelBroadcastRequest(openChannelBroadcastRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.BroadcastOpenChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BroadcastOpenChannelMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.BroadcastOpenChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiBroadcastOpenChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelBroadcastRequest** | [**OpenChannelBroadcastRequest**](OpenChannelBroadcastRequest.md) |  | 

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


## DeleteChannelMessageHistory

> CodeOnlyResponse DeleteChannelMessageHistory(ctx).ChannelMessageHistoryDeleteRequest(channelMessageHistoryDeleteRequest).Execute()

Delete server-side channel message history



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
	channelMessageHistoryDeleteRequest := *openapiclient.NewChannelMessageHistoryDeleteRequest(int32(123), "FromUserId_example", "ChannelId_example") // ChannelMessageHistoryDeleteRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.DeleteChannelMessageHistory(context.Background()).ChannelMessageHistoryDeleteRequest(channelMessageHistoryDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.DeleteChannelMessageHistory``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteChannelMessageHistory`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.DeleteChannelMessageHistory`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteChannelMessageHistoryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelMessageHistoryDeleteRequest** | [**ChannelMessageHistoryDeleteRequest**](ChannelMessageHistoryDeleteRequest.md) |  | 

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


## DeleteChannelTypeMessageMetadata

> CodeOnlyResponse DeleteChannelTypeMessageMetadata(ctx).ChannelTypeMessageMetadataDeleteRequest(channelTypeMessageMetadataDeleteRequest).Execute()

Delete message metadata



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
	channelTypeMessageMetadataDeleteRequest := *openapiclient.NewChannelTypeMessageMetadataDeleteRequest("MessageId_example", "UserId_example", int32(123), "ChannelId_example", []string{"Keys_example"}) // ChannelTypeMessageMetadataDeleteRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.DeleteChannelTypeMessageMetadata(context.Background()).ChannelTypeMessageMetadataDeleteRequest(channelTypeMessageMetadataDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.DeleteChannelTypeMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteChannelTypeMessageMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.DeleteChannelTypeMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteChannelTypeMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeMessageMetadataDeleteRequest** | [**ChannelTypeMessageMetadataDeleteRequest**](ChannelTypeMessageMetadataDeleteRequest.md) |  | 

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


## DeleteCommunityChannelMessageMetadata

> CodeOnlyResponse DeleteCommunityChannelMessageMetadata(ctx).CommunityChannelMessageMetadataDeleteRequest(communityChannelMessageMetadataDeleteRequest).Execute()

Delete community-channel message metadata keys

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
	communityChannelMessageMetadataDeleteRequest := *openapiclient.NewCommunityChannelMessageMetadataDeleteRequest("MessageId_example", "UserId_example", "ChannelId_example", []string{"Keys_example"}) // CommunityChannelMessageMetadataDeleteRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.DeleteCommunityChannelMessageMetadata(context.Background()).CommunityChannelMessageMetadataDeleteRequest(communityChannelMessageMetadataDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.DeleteCommunityChannelMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteCommunityChannelMessageMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.DeleteCommunityChannelMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteCommunityChannelMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMessageMetadataDeleteRequest** | [**CommunityChannelMessageMetadataDeleteRequest**](CommunityChannelMessageMetadataDeleteRequest.md) |  | 

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


## DeleteMessage

> CodeOnlyResponse DeleteMessage(ctx).MessageDeleteRequest(messageDeleteRequest).Execute()

Delete a message (recall)



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
	messageDeleteRequest := *openapiclient.NewMessageDeleteRequest("FromUserId_example", int32(123), "ChannelId_example", "MessageId_example") // MessageDeleteRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.DeleteMessage(context.Background()).MessageDeleteRequest(messageDeleteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.DeleteMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.DeleteMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDeleteMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageDeleteRequest** | [**MessageDeleteRequest**](MessageDeleteRequest.md) |  | 

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


## ListChannelTypeMessageMetadata

> ChannelTypeMessageMetadataListResponse ListChannelTypeMessageMetadata(ctx).ChannelTypeMessageMetadataListRequest(channelTypeMessageMetadataListRequest).Execute()

Get message metadata



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
	channelTypeMessageMetadataListRequest := *openapiclient.NewChannelTypeMessageMetadataListRequest("MessageId_example") // ChannelTypeMessageMetadataListRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.ListChannelTypeMessageMetadata(context.Background()).ChannelTypeMessageMetadataListRequest(channelTypeMessageMetadataListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.ListChannelTypeMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListChannelTypeMessageMetadata`: ChannelTypeMessageMetadataListResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.ListChannelTypeMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListChannelTypeMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelTypeMessageMetadataListRequest** | [**ChannelTypeMessageMetadataListRequest**](ChannelTypeMessageMetadataListRequest.md) |  | 

### Return type

[**ChannelTypeMessageMetadataListResponse**](ChannelTypeMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCommunityChannelMessageMetadata

> CommunityChannelMessageMetadataListResponse ListCommunityChannelMessageMetadata(ctx).CommunityChannelMessageMetadataListRequest(communityChannelMessageMetadataListRequest).Execute()

List community-channel message metadata

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
	communityChannelMessageMetadataListRequest := *openapiclient.NewCommunityChannelMessageMetadataListRequest("MessageId_example", "ChannelId_example") // CommunityChannelMessageMetadataListRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.ListCommunityChannelMessageMetadata(context.Background()).CommunityChannelMessageMetadataListRequest(communityChannelMessageMetadataListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.ListCommunityChannelMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCommunityChannelMessageMetadata`: CommunityChannelMessageMetadataListResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.ListCommunityChannelMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCommunityChannelMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMessageMetadataListRequest** | [**CommunityChannelMessageMetadataListRequest**](CommunityChannelMessageMetadataListRequest.md) |  | 

### Return type

[**CommunityChannelMessageMetadataListResponse**](CommunityChannelMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SendCommunityChannelMessage

> ChannelMessageSendResponse SendCommunityChannelMessage(ctx).CommunityChannelMessageSendRequest(communityChannelMessageSendRequest).Execute()

Send a community channel message



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
	communityChannelMessageSendRequest := *openapiclient.NewCommunityChannelMessageSendRequest("FromUserId_example", []string{"ToChannelIds_example"}, "MessageType_example", "Content_example") // CommunityChannelMessageSendRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SendCommunityChannelMessage(context.Background()).CommunityChannelMessageSendRequest(communityChannelMessageSendRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SendCommunityChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendCommunityChannelMessage`: ChannelMessageSendResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SendCommunityChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendCommunityChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMessageSendRequest** | [**CommunityChannelMessageSendRequest**](CommunityChannelMessageSendRequest.md) |  | 

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SendDirectChannelMessage

> UserMessageSendResponse SendDirectChannelMessage(ctx).DirectChannelMessageSendRequest(directChannelMessageSendRequest).Execute()

Send a direct message



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
	directChannelMessageSendRequest := *openapiclient.NewDirectChannelMessageSendRequest("FromUserId_example", []string{"ToUserIds_example"}, "MessageType_example", "Content_example") // DirectChannelMessageSendRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SendDirectChannelMessage(context.Background()).DirectChannelMessageSendRequest(directChannelMessageSendRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SendDirectChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendDirectChannelMessage`: UserMessageSendResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SendDirectChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendDirectChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **directChannelMessageSendRequest** | [**DirectChannelMessageSendRequest**](DirectChannelMessageSendRequest.md) |  | 

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


## SendGroupChannelMessage

> ChannelMessageSendResponse SendGroupChannelMessage(ctx).GroupChannelMessageSendRequest(groupChannelMessageSendRequest).Execute()

Send a group message



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
	groupChannelMessageSendRequest := *openapiclient.NewGroupChannelMessageSendRequest("FromUserId_example", []string{"ToChannelIds_example"}, "MessageType_example", "Content_example") // GroupChannelMessageSendRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SendGroupChannelMessage(context.Background()).GroupChannelMessageSendRequest(groupChannelMessageSendRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SendGroupChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendGroupChannelMessage`: ChannelMessageSendResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SendGroupChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendGroupChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMessageSendRequest** | [**GroupChannelMessageSendRequest**](GroupChannelMessageSendRequest.md) |  | 

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SendOpenChannelMessage

> ChannelMessageSendResponse SendOpenChannelMessage(ctx).OpenChannelMessageSendRequest(openChannelMessageSendRequest).Execute()

Send an open channel message



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
	openChannelMessageSendRequest := *openapiclient.NewOpenChannelMessageSendRequest("FromUserId_example", []string{"ToChannelIds_example"}, "MessageType_example", "Content_example") // OpenChannelMessageSendRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SendOpenChannelMessage(context.Background()).OpenChannelMessageSendRequest(openChannelMessageSendRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SendOpenChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendOpenChannelMessage`: ChannelMessageSendResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SendOpenChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSendOpenChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelMessageSendRequest** | [**OpenChannelMessageSendRequest**](OpenChannelMessageSendRequest.md) |  | 

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SetChannelTypeMessageMetadata

> CodeOnlyResponse SetChannelTypeMessageMetadata(ctx).MessageMetadataSetRequest(messageMetadataSetRequest).Execute()

Set message metadata



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
	messageMetadataSetRequest := *openapiclient.NewMessageMetadataSetRequest("MessageId_example", "UserId_example", int32(123), "ChannelId_example", map[string]string{"key": "Inner_example"}) // MessageMetadataSetRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SetChannelTypeMessageMetadata(context.Background()).MessageMetadataSetRequest(messageMetadataSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SetChannelTypeMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetChannelTypeMessageMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SetChannelTypeMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetChannelTypeMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageMetadataSetRequest** | [**MessageMetadataSetRequest**](MessageMetadataSetRequest.md) |  | 

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


## SetCommunityChannelMessageMetadata

> CodeOnlyResponse SetCommunityChannelMessageMetadata(ctx).CommunityChannelMessageMetadataSetRequest(communityChannelMessageMetadataSetRequest).Execute()

Set community-channel message metadata

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
	communityChannelMessageMetadataSetRequest := *openapiclient.NewCommunityChannelMessageMetadataSetRequest("MessageId_example", "UserId_example", "ChannelId_example", map[string]string{"key": "Inner_example"}) // CommunityChannelMessageMetadataSetRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.SetCommunityChannelMessageMetadata(context.Background()).CommunityChannelMessageMetadataSetRequest(communityChannelMessageMetadataSetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.SetCommunityChannelMessageMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetCommunityChannelMessageMetadata`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.SetCommunityChannelMessageMetadata`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiSetCommunityChannelMessageMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMessageMetadataSetRequest** | [**CommunityChannelMessageMetadataSetRequest**](CommunityChannelMessageMetadataSetRequest.md) |  | 

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


## UpdateCommunityChannelMessage

> CodeOnlyResponse UpdateCommunityChannelMessage(ctx).CommunityChannelMessageUpdateRequest(communityChannelMessageUpdateRequest).Execute()

Update community-channel message

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
	communityChannelMessageUpdateRequest := *openapiclient.NewCommunityChannelMessageUpdateRequest("ChannelId_example", "FromUserId_example", "MessageId_example", "Content_example") // CommunityChannelMessageUpdateRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.UpdateCommunityChannelMessage(context.Background()).CommunityChannelMessageUpdateRequest(communityChannelMessageUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.UpdateCommunityChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateCommunityChannelMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.UpdateCommunityChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateCommunityChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communityChannelMessageUpdateRequest** | [**CommunityChannelMessageUpdateRequest**](CommunityChannelMessageUpdateRequest.md) |  | 

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


## UpdateDirectChannelMessage

> CodeOnlyResponse UpdateDirectChannelMessage(ctx).DirectChannelMessageUpdateRequest(directChannelMessageUpdateRequest).Execute()

Update direct-channel message

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
	directChannelMessageUpdateRequest := *openapiclient.NewDirectChannelMessageUpdateRequest("FromUserId_example", "TargetId_example", "MessageId_example", "Content_example") // DirectChannelMessageUpdateRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.UpdateDirectChannelMessage(context.Background()).DirectChannelMessageUpdateRequest(directChannelMessageUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.UpdateDirectChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateDirectChannelMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.UpdateDirectChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateDirectChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **directChannelMessageUpdateRequest** | [**DirectChannelMessageUpdateRequest**](DirectChannelMessageUpdateRequest.md) |  | 

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


## UpdateGroupChannelMessage

> CodeOnlyResponse UpdateGroupChannelMessage(ctx).GroupChannelMessageUpdateRequest(groupChannelMessageUpdateRequest).Execute()

Update group-channel message

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
	groupChannelMessageUpdateRequest := *openapiclient.NewGroupChannelMessageUpdateRequest("FromUserId_example", "ChannelId_example", "MessageId_example", "Content_example") // GroupChannelMessageUpdateRequest | 

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
	resp, r, err := apiClient.MessageManagementAPI.UpdateGroupChannelMessage(context.Background()).GroupChannelMessageUpdateRequest(groupChannelMessageUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MessageManagementAPI.UpdateGroupChannelMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateGroupChannelMessage`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `MessageManagementAPI.UpdateGroupChannelMessage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiUpdateGroupChannelMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupChannelMessageUpdateRequest** | [**GroupChannelMessageUpdateRequest**](GroupChannelMessageUpdateRequest.md) |  | 

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


# OpenChannelParticipantsModerationAPI
All requests use the primary/backup domains configured by the caller.

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddOpenChannelFreezeList**](OpenChannelParticipantsModerationAPI.md#AddOpenChannelFreezeList) | **Post** /v4/open-channel/freeze-list/add | Freeze an open channel
[**AddOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationAPI.md#AddOpenChannelGlobalMuteList) | **Post** /v4/open-channel/global-mute-list/add | Mute a user globally
[**AddOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationAPI.md#AddOpenChannelParticipantAllowedSenderList) | **Post** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list
[**AddOpenChannelParticipantBanList**](OpenChannelParticipantsModerationAPI.md#AddOpenChannelParticipantBanList) | **Post** /v4/open-channel/participant/ban-list/add | Ban a participant
[**AddOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationAPI.md#AddOpenChannelParticipantMuteList) | **Post** /v4/open-channel/participant/mute-list/add | Mute a participant
[**CheckOpenChannelFreeze**](OpenChannelParticipantsModerationAPI.md#CheckOpenChannelFreeze) | **Post** /v4/open-channel/freeze/check | Check open channel freeze status
[**CheckOpenChannelParticipantsExist**](OpenChannelParticipantsModerationAPI.md#CheckOpenChannelParticipantsExist) | **Post** /v4/open-channel/participant/exist | Batch check participants
[**GetOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationAPI.md#GetOpenChannelGlobalMuteList) | **Post** /v4/open-channel/global-mute-list/get | List globally muted users
[**GetOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationAPI.md#GetOpenChannelParticipantAllowedSenderList) | **Post** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list
[**GetOpenChannelParticipantBanList**](OpenChannelParticipantsModerationAPI.md#GetOpenChannelParticipantBanList) | **Post** /v4/open-channel/participant/ban-list/get | List banned participants
[**GetOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationAPI.md#GetOpenChannelParticipantMuteList) | **Post** /v4/open-channel/participant/mute-list/get | List muted participants
[**ListFrozenOpenChannels**](OpenChannelParticipantsModerationAPI.md#ListFrozenOpenChannels) | **Post** /v4/open-channel/freeze-list/get | List frozen open channels
[**ListOpenChannelParticipants**](OpenChannelParticipantsModerationAPI.md#ListOpenChannelParticipants) | **Post** /v4/open-channel/participant/list | List participants
[**RemoveOpenChannelFreezeList**](OpenChannelParticipantsModerationAPI.md#RemoveOpenChannelFreezeList) | **Post** /v4/open-channel/freeze-list/remove | Unfreeze an open channel
[**RemoveOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationAPI.md#RemoveOpenChannelGlobalMuteList) | **Post** /v4/open-channel/global-mute-list/remove | Unmute a user globally
[**RemoveOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationAPI.md#RemoveOpenChannelParticipantAllowedSenderList) | **Post** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list
[**RemoveOpenChannelParticipantBanList**](OpenChannelParticipantsModerationAPI.md#RemoveOpenChannelParticipantBanList) | **Post** /v4/open-channel/participant/ban-list/remove | Unban a participant
[**RemoveOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationAPI.md#RemoveOpenChannelParticipantMuteList) | **Post** /v4/open-channel/participant/mute-list/remove | Unmute a participant



## AddOpenChannelFreezeList

> CodeOnlyResponse AddOpenChannelFreezeList(ctx).OpenChannelFreezeListUpdateRequest(openChannelFreezeListUpdateRequest).Execute()

Freeze an open channel



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
	openChannelFreezeListUpdateRequest := *openapiclient.NewOpenChannelFreezeListUpdateRequest("ChannelId_example") // OpenChannelFreezeListUpdateRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.AddOpenChannelFreezeList(context.Background()).OpenChannelFreezeListUpdateRequest(openChannelFreezeListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.AddOpenChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelFreezeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.AddOpenChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelFreezeListUpdateRequest** | [**OpenChannelFreezeListUpdateRequest**](OpenChannelFreezeListUpdateRequest.md) |  | 

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


## AddOpenChannelGlobalMuteList

> CodeOnlyResponse AddOpenChannelGlobalMuteList(ctx).OpenChannelGlobalMuteListAddRequest(openChannelGlobalMuteListAddRequest).Execute()

Mute a user globally



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
	openChannelGlobalMuteListAddRequest := *openapiclient.NewOpenChannelGlobalMuteListAddRequest([]string{"ParticipantIds_example"}, int32(123)) // OpenChannelGlobalMuteListAddRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.AddOpenChannelGlobalMuteList(context.Background()).OpenChannelGlobalMuteListAddRequest(openChannelGlobalMuteListAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.AddOpenChannelGlobalMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelGlobalMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.AddOpenChannelGlobalMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelGlobalMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelGlobalMuteListAddRequest** | [**OpenChannelGlobalMuteListAddRequest**](OpenChannelGlobalMuteListAddRequest.md) |  | 

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


## AddOpenChannelParticipantAllowedSenderList

> CodeOnlyResponse AddOpenChannelParticipantAllowedSenderList(ctx).OpenChannelAllowedSenderListUpdateRequest(openChannelAllowedSenderListUpdateRequest).Execute()

Add to allowed senders list



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
	openChannelAllowedSenderListUpdateRequest := *openapiclient.NewOpenChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantAllowedSenderList(context.Background()).OpenChannelAllowedSenderListUpdateRequest(openChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelParticipantAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelParticipantAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelAllowedSenderListUpdateRequest** | [**OpenChannelAllowedSenderListUpdateRequest**](OpenChannelAllowedSenderListUpdateRequest.md) |  | 

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


## AddOpenChannelParticipantBanList

> CodeOnlyResponse AddOpenChannelParticipantBanList(ctx).OpenChannelParticipantMuteListAddRequest(openChannelParticipantMuteListAddRequest).Execute()

Ban a participant



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
	openChannelParticipantMuteListAddRequest := *openapiclient.NewOpenChannelParticipantMuteListAddRequest("ChannelId_example", []string{"ParticipantIds_example"}, int32(123)) // OpenChannelParticipantMuteListAddRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantBanList(context.Background()).OpenChannelParticipantMuteListAddRequest(openChannelParticipantMuteListAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantBanList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelParticipantBanList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantBanList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelParticipantBanListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantMuteListAddRequest** | [**OpenChannelParticipantMuteListAddRequest**](OpenChannelParticipantMuteListAddRequest.md) |  | 

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


## AddOpenChannelParticipantMuteList

> CodeOnlyResponse AddOpenChannelParticipantMuteList(ctx).OpenChannelParticipantMuteListAddRequest(openChannelParticipantMuteListAddRequest).Execute()

Mute a participant



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
	openChannelParticipantMuteListAddRequest := *openapiclient.NewOpenChannelParticipantMuteListAddRequest("ChannelId_example", []string{"ParticipantIds_example"}, int32(123)) // OpenChannelParticipantMuteListAddRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantMuteList(context.Background()).OpenChannelParticipantMuteListAddRequest(openChannelParticipantMuteListAddRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AddOpenChannelParticipantMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.AddOpenChannelParticipantMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddOpenChannelParticipantMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantMuteListAddRequest** | [**OpenChannelParticipantMuteListAddRequest**](OpenChannelParticipantMuteListAddRequest.md) |  | 

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


## CheckOpenChannelFreeze

> OpenChannelFreezeCheckResponse CheckOpenChannelFreeze(ctx).OpenChannelFreezeCheckRequest(openChannelFreezeCheckRequest).Execute()

Check open channel freeze status



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
	openChannelFreezeCheckRequest := *openapiclient.NewOpenChannelFreezeCheckRequest("ChannelId_example") // OpenChannelFreezeCheckRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.CheckOpenChannelFreeze(context.Background()).OpenChannelFreezeCheckRequest(openChannelFreezeCheckRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.CheckOpenChannelFreeze``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CheckOpenChannelFreeze`: OpenChannelFreezeCheckResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.CheckOpenChannelFreeze`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCheckOpenChannelFreezeRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelFreezeCheckRequest** | [**OpenChannelFreezeCheckRequest**](OpenChannelFreezeCheckRequest.md) |  | 

### Return type

[**OpenChannelFreezeCheckResponse**](OpenChannelFreezeCheckResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CheckOpenChannelParticipantsExist

> OpenChannelParticipantExistResponse CheckOpenChannelParticipantsExist(ctx).OpenChannelParticipantExistRequest(openChannelParticipantExistRequest).Execute()

Batch check participants



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
	openChannelParticipantExistRequest := *openapiclient.NewOpenChannelParticipantExistRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelParticipantExistRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.CheckOpenChannelParticipantsExist(context.Background()).OpenChannelParticipantExistRequest(openChannelParticipantExistRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.CheckOpenChannelParticipantsExist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CheckOpenChannelParticipantsExist`: OpenChannelParticipantExistResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.CheckOpenChannelParticipantsExist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCheckOpenChannelParticipantsExistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantExistRequest** | [**OpenChannelParticipantExistRequest**](OpenChannelParticipantExistRequest.md) |  | 

### Return type

[**OpenChannelParticipantExistResponse**](OpenChannelParticipantExistResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetOpenChannelGlobalMuteList

> OpenChannelParticipantMuteListGetResponse GetOpenChannelGlobalMuteList(ctx).Body(body).Execute()

List globally muted users



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
	body := map[string]interface{}{ ... } // map[string]interface{} | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.GetOpenChannelGlobalMuteList(context.Background()).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.GetOpenChannelGlobalMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelGlobalMuteList`: OpenChannelParticipantMuteListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.GetOpenChannelGlobalMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelGlobalMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **map[string]interface{}** |  | 

### Return type

[**OpenChannelParticipantMuteListGetResponse**](OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetOpenChannelParticipantAllowedSenderList

> OpenChannelAllowedSenderListGetResponse GetOpenChannelParticipantAllowedSenderList(ctx).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()

Query allowed senders list



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
	openChannelParticipantListByChannelRequest := *openapiclient.NewOpenChannelParticipantListByChannelRequest("ChannelId_example") // OpenChannelParticipantListByChannelRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantAllowedSenderList(context.Background()).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelParticipantAllowedSenderList`: OpenChannelAllowedSenderListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelParticipantAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantListByChannelRequest** | [**OpenChannelParticipantListByChannelRequest**](OpenChannelParticipantListByChannelRequest.md) |  | 

### Return type

[**OpenChannelAllowedSenderListGetResponse**](OpenChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetOpenChannelParticipantBanList

> OpenChannelParticipantBanListGetResponse GetOpenChannelParticipantBanList(ctx).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()

List banned participants



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
	openChannelParticipantListByChannelRequest := *openapiclient.NewOpenChannelParticipantListByChannelRequest("ChannelId_example") // OpenChannelParticipantListByChannelRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantBanList(context.Background()).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantBanList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelParticipantBanList`: OpenChannelParticipantBanListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantBanList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelParticipantBanListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantListByChannelRequest** | [**OpenChannelParticipantListByChannelRequest**](OpenChannelParticipantListByChannelRequest.md) |  | 

### Return type

[**OpenChannelParticipantBanListGetResponse**](OpenChannelParticipantBanListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetOpenChannelParticipantMuteList

> OpenChannelParticipantMuteListGetResponse GetOpenChannelParticipantMuteList(ctx).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()

List muted participants



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
	openChannelParticipantListByChannelRequest := *openapiclient.NewOpenChannelParticipantListByChannelRequest("ChannelId_example") // OpenChannelParticipantListByChannelRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantMuteList(context.Background()).OpenChannelParticipantListByChannelRequest(openChannelParticipantListByChannelRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetOpenChannelParticipantMuteList`: OpenChannelParticipantMuteListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.GetOpenChannelParticipantMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetOpenChannelParticipantMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantListByChannelRequest** | [**OpenChannelParticipantListByChannelRequest**](OpenChannelParticipantListByChannelRequest.md) |  | 

### Return type

[**OpenChannelParticipantMuteListGetResponse**](OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListFrozenOpenChannels

> OpenChannelFreezeListGetResponse ListFrozenOpenChannels(ctx).OpenChannelFreezeListGetRequest(openChannelFreezeListGetRequest).Execute()

List frozen open channels



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
	openChannelFreezeListGetRequest := *openapiclient.NewOpenChannelFreezeListGetRequest() // OpenChannelFreezeListGetRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.ListFrozenOpenChannels(context.Background()).OpenChannelFreezeListGetRequest(openChannelFreezeListGetRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.ListFrozenOpenChannels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListFrozenOpenChannels`: OpenChannelFreezeListGetResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.ListFrozenOpenChannels`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListFrozenOpenChannelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelFreezeListGetRequest** | [**OpenChannelFreezeListGetRequest**](OpenChannelFreezeListGetRequest.md) |  | 

### Return type

[**OpenChannelFreezeListGetResponse**](OpenChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListOpenChannelParticipants

> OpenChannelParticipantListResponse ListOpenChannelParticipants(ctx).OpenChannelParticipantListRequest(openChannelParticipantListRequest).Execute()

List participants



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
	openChannelParticipantListRequest := *openapiclient.NewOpenChannelParticipantListRequest("ChannelId_example") // OpenChannelParticipantListRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.ListOpenChannelParticipants(context.Background()).OpenChannelParticipantListRequest(openChannelParticipantListRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.ListOpenChannelParticipants``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListOpenChannelParticipants`: OpenChannelParticipantListResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.ListOpenChannelParticipants`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListOpenChannelParticipantsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantListRequest** | [**OpenChannelParticipantListRequest**](OpenChannelParticipantListRequest.md) |  | 

### Return type

[**OpenChannelParticipantListResponse**](OpenChannelParticipantListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveOpenChannelFreezeList

> CodeOnlyResponse RemoveOpenChannelFreezeList(ctx).OpenChannelFreezeListUpdateRequest(openChannelFreezeListUpdateRequest).Execute()

Unfreeze an open channel



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
	openChannelFreezeListUpdateRequest := *openapiclient.NewOpenChannelFreezeListUpdateRequest("ChannelId_example") // OpenChannelFreezeListUpdateRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.RemoveOpenChannelFreezeList(context.Background()).OpenChannelFreezeListUpdateRequest(openChannelFreezeListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.RemoveOpenChannelFreezeList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelFreezeList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.RemoveOpenChannelFreezeList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelFreezeListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelFreezeListUpdateRequest** | [**OpenChannelFreezeListUpdateRequest**](OpenChannelFreezeListUpdateRequest.md) |  | 

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


## RemoveOpenChannelGlobalMuteList

> CodeOnlyResponse RemoveOpenChannelGlobalMuteList(ctx).OpenChannelGlobalMuteListRemoveRequest(openChannelGlobalMuteListRemoveRequest).Execute()

Unmute a user globally



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
	openChannelGlobalMuteListRemoveRequest := *openapiclient.NewOpenChannelGlobalMuteListRemoveRequest([]string{"ParticipantIds_example"}) // OpenChannelGlobalMuteListRemoveRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.RemoveOpenChannelGlobalMuteList(context.Background()).OpenChannelGlobalMuteListRemoveRequest(openChannelGlobalMuteListRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.RemoveOpenChannelGlobalMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelGlobalMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.RemoveOpenChannelGlobalMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelGlobalMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelGlobalMuteListRemoveRequest** | [**OpenChannelGlobalMuteListRemoveRequest**](OpenChannelGlobalMuteListRemoveRequest.md) |  | 

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


## RemoveOpenChannelParticipantAllowedSenderList

> CodeOnlyResponse RemoveOpenChannelParticipantAllowedSenderList(ctx).OpenChannelAllowedSenderListUpdateRequest(openChannelAllowedSenderListUpdateRequest).Execute()

Remove from allowed senders list



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
	openChannelAllowedSenderListUpdateRequest := *openapiclient.NewOpenChannelAllowedSenderListUpdateRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelAllowedSenderListUpdateRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantAllowedSenderList(context.Background()).OpenChannelAllowedSenderListUpdateRequest(openChannelAllowedSenderListUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantAllowedSenderList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelParticipantAllowedSenderList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantAllowedSenderList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelParticipantAllowedSenderListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelAllowedSenderListUpdateRequest** | [**OpenChannelAllowedSenderListUpdateRequest**](OpenChannelAllowedSenderListUpdateRequest.md) |  | 

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


## RemoveOpenChannelParticipantBanList

> CodeOnlyResponse RemoveOpenChannelParticipantBanList(ctx).OpenChannelParticipantMuteListRemoveRequest(openChannelParticipantMuteListRemoveRequest).Execute()

Unban a participant



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
	openChannelParticipantMuteListRemoveRequest := *openapiclient.NewOpenChannelParticipantMuteListRemoveRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelParticipantMuteListRemoveRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantBanList(context.Background()).OpenChannelParticipantMuteListRemoveRequest(openChannelParticipantMuteListRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantBanList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelParticipantBanList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantBanList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelParticipantBanListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantMuteListRemoveRequest** | [**OpenChannelParticipantMuteListRemoveRequest**](OpenChannelParticipantMuteListRemoveRequest.md) |  | 

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


## RemoveOpenChannelParticipantMuteList

> CodeOnlyResponse RemoveOpenChannelParticipantMuteList(ctx).OpenChannelParticipantMuteListRemoveRequest(openChannelParticipantMuteListRemoveRequest).Execute()

Unmute a participant



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
	openChannelParticipantMuteListRemoveRequest := *openapiclient.NewOpenChannelParticipantMuteListRemoveRequest("ChannelId_example", []string{"ParticipantIds_example"}) // OpenChannelParticipantMuteListRemoveRequest | 

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
	resp, r, err := apiClient.OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantMuteList(context.Background()).OpenChannelParticipantMuteListRemoveRequest(openChannelParticipantMuteListRemoveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantMuteList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RemoveOpenChannelParticipantMuteList`: CodeOnlyResponse
	fmt.Fprintf(os.Stdout, "Response from `OpenChannelParticipantsModerationAPI.RemoveOpenChannelParticipantMuteList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRemoveOpenChannelParticipantMuteListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **openChannelParticipantMuteListRemoveRequest** | [**OpenChannelParticipantMuteListRemoveRequest**](OpenChannelParticipantMuteListRemoveRequest.md) |  | 

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


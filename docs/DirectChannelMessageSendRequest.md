# DirectChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. | 
**ToUserIds** | **[]string** | Recipient user IDs. Up to 1000 users are supported in a single request. | 
**MessageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Message content payload. Built-in message types should pass a JSON object serialized as a string. Maximum size is 128 KB. | 
**PushContent** | Pointer to **string** | Push notification text shown to offline recipients. Required for custom message types or notification/signal messages that need push delivery. | [optional] 
**PushData** | Pointer to **string** | Custom payload included in the push notification. Exposed as &#x60;appData&#x60; on iOS and Android. | [optional] 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] 
**Count** | Pointer to **int32** | Aligns with Java &#x60;DirectChannelMsgSendInput.count&#x60; (push/badge-related counter field name in server model). | [optional] 
**VerifyBlocklist** | Pointer to **int32** | Whether to filter recipients against the sender&#39;s blocklist. &#x60;0&#x60; means no filtering and &#x60;1&#x60; means filter blocked users out. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**ContentAvailable** | Pointer to **int32** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] 
**HasMetadata** | Pointer to **bool** | Whether to enable message metadata (message expansion) for this message. | [optional] 
**Metadata** | Pointer to **map[string]interface{}** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. | [optional] 
**DisablePush** | Pointer to **bool** | Whether to suppress push notifications for offline recipients. | [optional] 
**PushExt** | Pointer to **string** | Extended push configuration (JSON string as accepted by &#x60;DirectChannelMsgSendInput&#x60;). | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional] 
**NeedReadReceipt** | Pointer to **int32** | Whether to request read receipts for this persisted message. &#x60;1&#x60; requests read receipts and &#x60;0&#x60; disables them. | [optional] 

## Methods

### NewDirectChannelMessageSendRequest

`func NewDirectChannelMessageSendRequest(fromUserId string, toUserIds []string, messageType string, content string, ) *DirectChannelMessageSendRequest`

NewDirectChannelMessageSendRequest instantiates a new DirectChannelMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDirectChannelMessageSendRequestWithDefaults

`func NewDirectChannelMessageSendRequestWithDefaults() *DirectChannelMessageSendRequest`

NewDirectChannelMessageSendRequestWithDefaults instantiates a new DirectChannelMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *DirectChannelMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *DirectChannelMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *DirectChannelMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToUserIds

`func (o *DirectChannelMessageSendRequest) GetToUserIds() []string`

GetToUserIds returns the ToUserIds field if non-nil, zero value otherwise.

### GetToUserIdsOk

`func (o *DirectChannelMessageSendRequest) GetToUserIdsOk() (*[]string, bool)`

GetToUserIdsOk returns a tuple with the ToUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserIds

`func (o *DirectChannelMessageSendRequest) SetToUserIds(v []string)`

SetToUserIds sets ToUserIds field to given value.


### GetMessageType

`func (o *DirectChannelMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *DirectChannelMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *DirectChannelMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *DirectChannelMessageSendRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *DirectChannelMessageSendRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *DirectChannelMessageSendRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetPushContent

`func (o *DirectChannelMessageSendRequest) GetPushContent() string`

GetPushContent returns the PushContent field if non-nil, zero value otherwise.

### GetPushContentOk

`func (o *DirectChannelMessageSendRequest) GetPushContentOk() (*string, bool)`

GetPushContentOk returns a tuple with the PushContent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushContent

`func (o *DirectChannelMessageSendRequest) SetPushContent(v string)`

SetPushContent sets PushContent field to given value.

### HasPushContent

`func (o *DirectChannelMessageSendRequest) HasPushContent() bool`

HasPushContent returns a boolean if a field has been set.

### GetPushData

`func (o *DirectChannelMessageSendRequest) GetPushData() string`

GetPushData returns the PushData field if non-nil, zero value otherwise.

### GetPushDataOk

`func (o *DirectChannelMessageSendRequest) GetPushDataOk() (*string, bool)`

GetPushDataOk returns a tuple with the PushData field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushData

`func (o *DirectChannelMessageSendRequest) SetPushData(v string)`

SetPushData sets PushData field to given value.

### HasPushData

`func (o *DirectChannelMessageSendRequest) HasPushData() bool`

HasPushData returns a boolean if a field has been set.

### GetIsEchoToSender

`func (o *DirectChannelMessageSendRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *DirectChannelMessageSendRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *DirectChannelMessageSendRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *DirectChannelMessageSendRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.

### GetCount

`func (o *DirectChannelMessageSendRequest) GetCount() int32`

GetCount returns the Count field if non-nil, zero value otherwise.

### GetCountOk

`func (o *DirectChannelMessageSendRequest) GetCountOk() (*int32, bool)`

GetCountOk returns a tuple with the Count field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCount

`func (o *DirectChannelMessageSendRequest) SetCount(v int32)`

SetCount sets Count field to given value.

### HasCount

`func (o *DirectChannelMessageSendRequest) HasCount() bool`

HasCount returns a boolean if a field has been set.

### GetVerifyBlocklist

`func (o *DirectChannelMessageSendRequest) GetVerifyBlocklist() int32`

GetVerifyBlocklist returns the VerifyBlocklist field if non-nil, zero value otherwise.

### GetVerifyBlocklistOk

`func (o *DirectChannelMessageSendRequest) GetVerifyBlocklistOk() (*int32, bool)`

GetVerifyBlocklistOk returns a tuple with the VerifyBlocklist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerifyBlocklist

`func (o *DirectChannelMessageSendRequest) SetVerifyBlocklist(v int32)`

SetVerifyBlocklist sets VerifyBlocklist field to given value.

### HasVerifyBlocklist

`func (o *DirectChannelMessageSendRequest) HasVerifyBlocklist() bool`

HasVerifyBlocklist returns a boolean if a field has been set.

### GetShouldPersist

`func (o *DirectChannelMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *DirectChannelMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *DirectChannelMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *DirectChannelMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetContentAvailable

`func (o *DirectChannelMessageSendRequest) GetContentAvailable() int32`

GetContentAvailable returns the ContentAvailable field if non-nil, zero value otherwise.

### GetContentAvailableOk

`func (o *DirectChannelMessageSendRequest) GetContentAvailableOk() (*int32, bool)`

GetContentAvailableOk returns a tuple with the ContentAvailable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContentAvailable

`func (o *DirectChannelMessageSendRequest) SetContentAvailable(v int32)`

SetContentAvailable sets ContentAvailable field to given value.

### HasContentAvailable

`func (o *DirectChannelMessageSendRequest) HasContentAvailable() bool`

HasContentAvailable returns a boolean if a field has been set.

### GetHasMetadata

`func (o *DirectChannelMessageSendRequest) GetHasMetadata() bool`

GetHasMetadata returns the HasMetadata field if non-nil, zero value otherwise.

### GetHasMetadataOk

`func (o *DirectChannelMessageSendRequest) GetHasMetadataOk() (*bool, bool)`

GetHasMetadataOk returns a tuple with the HasMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMetadata

`func (o *DirectChannelMessageSendRequest) SetHasMetadata(v bool)`

SetHasMetadata sets HasMetadata field to given value.

### HasHasMetadata

`func (o *DirectChannelMessageSendRequest) HasHasMetadata() bool`

HasHasMetadata returns a boolean if a field has been set.

### GetMetadata

`func (o *DirectChannelMessageSendRequest) GetMetadata() map[string]interface{}`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *DirectChannelMessageSendRequest) GetMetadataOk() (*map[string]interface{}, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *DirectChannelMessageSendRequest) SetMetadata(v map[string]interface{})`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *DirectChannelMessageSendRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetDisablePush

`func (o *DirectChannelMessageSendRequest) GetDisablePush() bool`

GetDisablePush returns the DisablePush field if non-nil, zero value otherwise.

### GetDisablePushOk

`func (o *DirectChannelMessageSendRequest) GetDisablePushOk() (*bool, bool)`

GetDisablePushOk returns a tuple with the DisablePush field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisablePush

`func (o *DirectChannelMessageSendRequest) SetDisablePush(v bool)`

SetDisablePush sets DisablePush field to given value.

### HasDisablePush

`func (o *DirectChannelMessageSendRequest) HasDisablePush() bool`

HasDisablePush returns a boolean if a field has been set.

### GetPushExt

`func (o *DirectChannelMessageSendRequest) GetPushExt() string`

GetPushExt returns the PushExt field if non-nil, zero value otherwise.

### GetPushExtOk

`func (o *DirectChannelMessageSendRequest) GetPushExtOk() (*string, bool)`

GetPushExtOk returns a tuple with the PushExt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushExt

`func (o *DirectChannelMessageSendRequest) SetPushExt(v string)`

SetPushExt sets PushExt field to given value.

### HasPushExt

`func (o *DirectChannelMessageSendRequest) HasPushExt() bool`

HasPushExt returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *DirectChannelMessageSendRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *DirectChannelMessageSendRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *DirectChannelMessageSendRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *DirectChannelMessageSendRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.

### GetNeedReadReceipt

`func (o *DirectChannelMessageSendRequest) GetNeedReadReceipt() int32`

GetNeedReadReceipt returns the NeedReadReceipt field if non-nil, zero value otherwise.

### GetNeedReadReceiptOk

`func (o *DirectChannelMessageSendRequest) GetNeedReadReceiptOk() (*int32, bool)`

GetNeedReadReceiptOk returns a tuple with the NeedReadReceipt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedReadReceipt

`func (o *DirectChannelMessageSendRequest) SetNeedReadReceipt(v int32)`

SetNeedReadReceipt sets NeedReadReceipt field to given value.

### HasNeedReadReceipt

`func (o *DirectChannelMessageSendRequest) HasNeedReadReceipt() bool`

HasNeedReadReceipt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



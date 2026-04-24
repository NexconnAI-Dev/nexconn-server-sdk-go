# GroupChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. Server-side sending does not require the sender to be a group member, but push display works best when the sender has an access token. | 
**ToChannelIds** | **[]string** | Target group channel IDs. Up to 3 groups are supported per request. Targeted messages support only one group. | 
**ToUserIds** | Pointer to **[]string** | Recipient member user IDs for a targeted group message. Only effective when sending to a single group. | [optional] 
**MessageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | 
**PushContent** | Pointer to **string** | Push notification text for offline recipients. Optional for built-in user content messages and required for push-enabled custom or notification messages. | [optional] 
**PushData** | Pointer to **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on mobile push payloads. | [optional] 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the sent message to the sender&#39;s client while online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**HasMention** | Pointer to **int32** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional] 
**ContentAvailable** | Pointer to **int32** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] 
**HasMetadata** | Pointer to **bool** | Whether to enable message metadata for this message. Only effective when sending to a single group channel. | [optional] 
**Metadata** | Pointer to **map[string]interface{}** | Custom message metadata entries. Only effective when &#x60;hasMetadata&#x60; is &#x60;true&#x60; and the request targets a single group. | [optional] 
**DisablePush** | Pointer to **bool** | Whether to suppress push notifications. Only effective when the request targets a single group channel. | [optional] 
**PushExt** | Pointer to **string** | Extended push configuration (JSON string as accepted by &#x60;GroupChannelMsgSendInput&#x60;). | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional] 
**NeedReadReceipt** | Pointer to **int32** | Whether to request read receipts for this persisted message. &#x60;1&#x60; requests read receipts and &#x60;0&#x60; disables them. | [optional] 

## Methods

### NewGroupChannelMessageSendRequest

`func NewGroupChannelMessageSendRequest(fromUserId string, toChannelIds []string, messageType string, content string, ) *GroupChannelMessageSendRequest`

NewGroupChannelMessageSendRequest instantiates a new GroupChannelMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMessageSendRequestWithDefaults

`func NewGroupChannelMessageSendRequestWithDefaults() *GroupChannelMessageSendRequest`

NewGroupChannelMessageSendRequestWithDefaults instantiates a new GroupChannelMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *GroupChannelMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *GroupChannelMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *GroupChannelMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToChannelIds

`func (o *GroupChannelMessageSendRequest) GetToChannelIds() []string`

GetToChannelIds returns the ToChannelIds field if non-nil, zero value otherwise.

### GetToChannelIdsOk

`func (o *GroupChannelMessageSendRequest) GetToChannelIdsOk() (*[]string, bool)`

GetToChannelIdsOk returns a tuple with the ToChannelIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToChannelIds

`func (o *GroupChannelMessageSendRequest) SetToChannelIds(v []string)`

SetToChannelIds sets ToChannelIds field to given value.


### GetToUserIds

`func (o *GroupChannelMessageSendRequest) GetToUserIds() []string`

GetToUserIds returns the ToUserIds field if non-nil, zero value otherwise.

### GetToUserIdsOk

`func (o *GroupChannelMessageSendRequest) GetToUserIdsOk() (*[]string, bool)`

GetToUserIdsOk returns a tuple with the ToUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserIds

`func (o *GroupChannelMessageSendRequest) SetToUserIds(v []string)`

SetToUserIds sets ToUserIds field to given value.

### HasToUserIds

`func (o *GroupChannelMessageSendRequest) HasToUserIds() bool`

HasToUserIds returns a boolean if a field has been set.

### GetMessageType

`func (o *GroupChannelMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *GroupChannelMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *GroupChannelMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *GroupChannelMessageSendRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *GroupChannelMessageSendRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *GroupChannelMessageSendRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetPushContent

`func (o *GroupChannelMessageSendRequest) GetPushContent() string`

GetPushContent returns the PushContent field if non-nil, zero value otherwise.

### GetPushContentOk

`func (o *GroupChannelMessageSendRequest) GetPushContentOk() (*string, bool)`

GetPushContentOk returns a tuple with the PushContent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushContent

`func (o *GroupChannelMessageSendRequest) SetPushContent(v string)`

SetPushContent sets PushContent field to given value.

### HasPushContent

`func (o *GroupChannelMessageSendRequest) HasPushContent() bool`

HasPushContent returns a boolean if a field has been set.

### GetPushData

`func (o *GroupChannelMessageSendRequest) GetPushData() string`

GetPushData returns the PushData field if non-nil, zero value otherwise.

### GetPushDataOk

`func (o *GroupChannelMessageSendRequest) GetPushDataOk() (*string, bool)`

GetPushDataOk returns a tuple with the PushData field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushData

`func (o *GroupChannelMessageSendRequest) SetPushData(v string)`

SetPushData sets PushData field to given value.

### HasPushData

`func (o *GroupChannelMessageSendRequest) HasPushData() bool`

HasPushData returns a boolean if a field has been set.

### GetIsEchoToSender

`func (o *GroupChannelMessageSendRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *GroupChannelMessageSendRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *GroupChannelMessageSendRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *GroupChannelMessageSendRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.

### GetShouldPersist

`func (o *GroupChannelMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *GroupChannelMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *GroupChannelMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *GroupChannelMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetHasMention

`func (o *GroupChannelMessageSendRequest) GetHasMention() int32`

GetHasMention returns the HasMention field if non-nil, zero value otherwise.

### GetHasMentionOk

`func (o *GroupChannelMessageSendRequest) GetHasMentionOk() (*int32, bool)`

GetHasMentionOk returns a tuple with the HasMention field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMention

`func (o *GroupChannelMessageSendRequest) SetHasMention(v int32)`

SetHasMention sets HasMention field to given value.

### HasHasMention

`func (o *GroupChannelMessageSendRequest) HasHasMention() bool`

HasHasMention returns a boolean if a field has been set.

### GetContentAvailable

`func (o *GroupChannelMessageSendRequest) GetContentAvailable() int32`

GetContentAvailable returns the ContentAvailable field if non-nil, zero value otherwise.

### GetContentAvailableOk

`func (o *GroupChannelMessageSendRequest) GetContentAvailableOk() (*int32, bool)`

GetContentAvailableOk returns a tuple with the ContentAvailable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContentAvailable

`func (o *GroupChannelMessageSendRequest) SetContentAvailable(v int32)`

SetContentAvailable sets ContentAvailable field to given value.

### HasContentAvailable

`func (o *GroupChannelMessageSendRequest) HasContentAvailable() bool`

HasContentAvailable returns a boolean if a field has been set.

### GetHasMetadata

`func (o *GroupChannelMessageSendRequest) GetHasMetadata() bool`

GetHasMetadata returns the HasMetadata field if non-nil, zero value otherwise.

### GetHasMetadataOk

`func (o *GroupChannelMessageSendRequest) GetHasMetadataOk() (*bool, bool)`

GetHasMetadataOk returns a tuple with the HasMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMetadata

`func (o *GroupChannelMessageSendRequest) SetHasMetadata(v bool)`

SetHasMetadata sets HasMetadata field to given value.

### HasHasMetadata

`func (o *GroupChannelMessageSendRequest) HasHasMetadata() bool`

HasHasMetadata returns a boolean if a field has been set.

### GetMetadata

`func (o *GroupChannelMessageSendRequest) GetMetadata() map[string]interface{}`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *GroupChannelMessageSendRequest) GetMetadataOk() (*map[string]interface{}, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *GroupChannelMessageSendRequest) SetMetadata(v map[string]interface{})`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *GroupChannelMessageSendRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetDisablePush

`func (o *GroupChannelMessageSendRequest) GetDisablePush() bool`

GetDisablePush returns the DisablePush field if non-nil, zero value otherwise.

### GetDisablePushOk

`func (o *GroupChannelMessageSendRequest) GetDisablePushOk() (*bool, bool)`

GetDisablePushOk returns a tuple with the DisablePush field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisablePush

`func (o *GroupChannelMessageSendRequest) SetDisablePush(v bool)`

SetDisablePush sets DisablePush field to given value.

### HasDisablePush

`func (o *GroupChannelMessageSendRequest) HasDisablePush() bool`

HasDisablePush returns a boolean if a field has been set.

### GetPushExt

`func (o *GroupChannelMessageSendRequest) GetPushExt() string`

GetPushExt returns the PushExt field if non-nil, zero value otherwise.

### GetPushExtOk

`func (o *GroupChannelMessageSendRequest) GetPushExtOk() (*string, bool)`

GetPushExtOk returns a tuple with the PushExt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushExt

`func (o *GroupChannelMessageSendRequest) SetPushExt(v string)`

SetPushExt sets PushExt field to given value.

### HasPushExt

`func (o *GroupChannelMessageSendRequest) HasPushExt() bool`

HasPushExt returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *GroupChannelMessageSendRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *GroupChannelMessageSendRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *GroupChannelMessageSendRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *GroupChannelMessageSendRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.

### GetNeedReadReceipt

`func (o *GroupChannelMessageSendRequest) GetNeedReadReceipt() int32`

GetNeedReadReceipt returns the NeedReadReceipt field if non-nil, zero value otherwise.

### GetNeedReadReceiptOk

`func (o *GroupChannelMessageSendRequest) GetNeedReadReceiptOk() (*int32, bool)`

GetNeedReadReceiptOk returns a tuple with the NeedReadReceipt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedReadReceipt

`func (o *GroupChannelMessageSendRequest) SetNeedReadReceipt(v int32)`

SetNeedReadReceipt sets NeedReadReceipt field to given value.

### HasNeedReadReceipt

`func (o *GroupChannelMessageSendRequest) HasNeedReadReceipt() bool`

HasNeedReadReceipt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



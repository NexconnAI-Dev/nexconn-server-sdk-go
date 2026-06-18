# GroupChannelStreamMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. | 
**ToChannelId** | **string** | Target group channel ID. | 
**MessageType** | **string** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. | 
**Content** | [**StreamMessageContent**](StreamMessageContent.md) |  | 
**ToUserIds** | Pointer to **[]string** | Recipient member user IDs for a targeted group message. Up to 10 users. | [optional] 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**HasMention** | Pointer to **int32** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional] 
**Metadata** | Pointer to **map[string]string** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional] 

## Methods

### NewGroupChannelStreamMessageSendRequest

`func NewGroupChannelStreamMessageSendRequest(fromUserId string, toChannelId string, messageType string, content StreamMessageContent, ) *GroupChannelStreamMessageSendRequest`

NewGroupChannelStreamMessageSendRequest instantiates a new GroupChannelStreamMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelStreamMessageSendRequestWithDefaults

`func NewGroupChannelStreamMessageSendRequestWithDefaults() *GroupChannelStreamMessageSendRequest`

NewGroupChannelStreamMessageSendRequestWithDefaults instantiates a new GroupChannelStreamMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *GroupChannelStreamMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *GroupChannelStreamMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *GroupChannelStreamMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToChannelId

`func (o *GroupChannelStreamMessageSendRequest) GetToChannelId() string`

GetToChannelId returns the ToChannelId field if non-nil, zero value otherwise.

### GetToChannelIdOk

`func (o *GroupChannelStreamMessageSendRequest) GetToChannelIdOk() (*string, bool)`

GetToChannelIdOk returns a tuple with the ToChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToChannelId

`func (o *GroupChannelStreamMessageSendRequest) SetToChannelId(v string)`

SetToChannelId sets ToChannelId field to given value.


### GetMessageType

`func (o *GroupChannelStreamMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *GroupChannelStreamMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *GroupChannelStreamMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *GroupChannelStreamMessageSendRequest) GetContent() StreamMessageContent`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *GroupChannelStreamMessageSendRequest) GetContentOk() (*StreamMessageContent, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *GroupChannelStreamMessageSendRequest) SetContent(v StreamMessageContent)`

SetContent sets Content field to given value.


### GetToUserIds

`func (o *GroupChannelStreamMessageSendRequest) GetToUserIds() []string`

GetToUserIds returns the ToUserIds field if non-nil, zero value otherwise.

### GetToUserIdsOk

`func (o *GroupChannelStreamMessageSendRequest) GetToUserIdsOk() (*[]string, bool)`

GetToUserIdsOk returns a tuple with the ToUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserIds

`func (o *GroupChannelStreamMessageSendRequest) SetToUserIds(v []string)`

SetToUserIds sets ToUserIds field to given value.

### HasToUserIds

`func (o *GroupChannelStreamMessageSendRequest) HasToUserIds() bool`

HasToUserIds returns a boolean if a field has been set.

### GetIsEchoToSender

`func (o *GroupChannelStreamMessageSendRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *GroupChannelStreamMessageSendRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *GroupChannelStreamMessageSendRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *GroupChannelStreamMessageSendRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.

### GetShouldPersist

`func (o *GroupChannelStreamMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *GroupChannelStreamMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *GroupChannelStreamMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *GroupChannelStreamMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetHasMention

`func (o *GroupChannelStreamMessageSendRequest) GetHasMention() int32`

GetHasMention returns the HasMention field if non-nil, zero value otherwise.

### GetHasMentionOk

`func (o *GroupChannelStreamMessageSendRequest) GetHasMentionOk() (*int32, bool)`

GetHasMentionOk returns a tuple with the HasMention field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMention

`func (o *GroupChannelStreamMessageSendRequest) SetHasMention(v int32)`

SetHasMention sets HasMention field to given value.

### HasHasMention

`func (o *GroupChannelStreamMessageSendRequest) HasHasMention() bool`

HasHasMention returns a boolean if a field has been set.

### GetMetadata

`func (o *GroupChannelStreamMessageSendRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *GroupChannelStreamMessageSendRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *GroupChannelStreamMessageSendRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *GroupChannelStreamMessageSendRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *GroupChannelStreamMessageSendRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *GroupChannelStreamMessageSendRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *GroupChannelStreamMessageSendRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *GroupChannelStreamMessageSendRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



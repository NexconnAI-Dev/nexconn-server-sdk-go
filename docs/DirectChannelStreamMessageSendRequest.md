# DirectChannelStreamMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. | 
**ToUserId** | **string** | Recipient user ID. Only a single recipient is supported per stream message. | 
**MessageType** | **string** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. | 
**Content** | [**StreamMessageContent**](StreamMessageContent.md) |  | 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**Metadata** | Pointer to **map[string]string** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional] 

## Methods

### NewDirectChannelStreamMessageSendRequest

`func NewDirectChannelStreamMessageSendRequest(fromUserId string, toUserId string, messageType string, content StreamMessageContent, ) *DirectChannelStreamMessageSendRequest`

NewDirectChannelStreamMessageSendRequest instantiates a new DirectChannelStreamMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDirectChannelStreamMessageSendRequestWithDefaults

`func NewDirectChannelStreamMessageSendRequestWithDefaults() *DirectChannelStreamMessageSendRequest`

NewDirectChannelStreamMessageSendRequestWithDefaults instantiates a new DirectChannelStreamMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *DirectChannelStreamMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *DirectChannelStreamMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *DirectChannelStreamMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToUserId

`func (o *DirectChannelStreamMessageSendRequest) GetToUserId() string`

GetToUserId returns the ToUserId field if non-nil, zero value otherwise.

### GetToUserIdOk

`func (o *DirectChannelStreamMessageSendRequest) GetToUserIdOk() (*string, bool)`

GetToUserIdOk returns a tuple with the ToUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserId

`func (o *DirectChannelStreamMessageSendRequest) SetToUserId(v string)`

SetToUserId sets ToUserId field to given value.


### GetMessageType

`func (o *DirectChannelStreamMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *DirectChannelStreamMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *DirectChannelStreamMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *DirectChannelStreamMessageSendRequest) GetContent() StreamMessageContent`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *DirectChannelStreamMessageSendRequest) GetContentOk() (*StreamMessageContent, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *DirectChannelStreamMessageSendRequest) SetContent(v StreamMessageContent)`

SetContent sets Content field to given value.


### GetIsEchoToSender

`func (o *DirectChannelStreamMessageSendRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *DirectChannelStreamMessageSendRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *DirectChannelStreamMessageSendRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *DirectChannelStreamMessageSendRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.

### GetShouldPersist

`func (o *DirectChannelStreamMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *DirectChannelStreamMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *DirectChannelStreamMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *DirectChannelStreamMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetMetadata

`func (o *DirectChannelStreamMessageSendRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *DirectChannelStreamMessageSendRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *DirectChannelStreamMessageSendRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *DirectChannelStreamMessageSendRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *DirectChannelStreamMessageSendRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *DirectChannelStreamMessageSendRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *DirectChannelStreamMessageSendRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *DirectChannelStreamMessageSendRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



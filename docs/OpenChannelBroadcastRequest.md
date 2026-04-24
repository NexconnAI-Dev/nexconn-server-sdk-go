# OpenChannelBroadcastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. | 
**MessageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Broadcast message payload serialized as a string. Maximum size is 128 KB. | 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the broadcast message to the sender&#39;s client while the sender is online. | [optional] 

## Methods

### NewOpenChannelBroadcastRequest

`func NewOpenChannelBroadcastRequest(fromUserId string, messageType string, content string, ) *OpenChannelBroadcastRequest`

NewOpenChannelBroadcastRequest instantiates a new OpenChannelBroadcastRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelBroadcastRequestWithDefaults

`func NewOpenChannelBroadcastRequestWithDefaults() *OpenChannelBroadcastRequest`

NewOpenChannelBroadcastRequestWithDefaults instantiates a new OpenChannelBroadcastRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *OpenChannelBroadcastRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *OpenChannelBroadcastRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *OpenChannelBroadcastRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetMessageType

`func (o *OpenChannelBroadcastRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *OpenChannelBroadcastRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *OpenChannelBroadcastRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *OpenChannelBroadcastRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *OpenChannelBroadcastRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *OpenChannelBroadcastRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetIsEchoToSender

`func (o *OpenChannelBroadcastRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *OpenChannelBroadcastRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *OpenChannelBroadcastRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *OpenChannelBroadcastRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



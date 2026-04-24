# MessageMetadataSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**UserId** | **string** |  | 
**ChannelType** | **int32** | Supports &#x60;1&#x60; and &#x60;3&#x60;. | 
**ChannelId** | **string** |  | 
**Metadata** | **map[string]string** | Message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 100 entries.  | 
**IsEchoToSender** | Pointer to **int32** |  | [optional] 

## Methods

### NewMessageMetadataSetRequest

`func NewMessageMetadataSetRequest(messageId string, userId string, channelType int32, channelId string, metadata map[string]string, ) *MessageMetadataSetRequest`

NewMessageMetadataSetRequest instantiates a new MessageMetadataSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMessageMetadataSetRequestWithDefaults

`func NewMessageMetadataSetRequestWithDefaults() *MessageMetadataSetRequest`

NewMessageMetadataSetRequestWithDefaults instantiates a new MessageMetadataSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *MessageMetadataSetRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *MessageMetadataSetRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *MessageMetadataSetRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetUserId

`func (o *MessageMetadataSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *MessageMetadataSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *MessageMetadataSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelType

`func (o *MessageMetadataSetRequest) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *MessageMetadataSetRequest) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *MessageMetadataSetRequest) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.


### GetChannelId

`func (o *MessageMetadataSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *MessageMetadataSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *MessageMetadataSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetMetadata

`func (o *MessageMetadataSetRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *MessageMetadataSetRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *MessageMetadataSetRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.


### GetIsEchoToSender

`func (o *MessageMetadataSetRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *MessageMetadataSetRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *MessageMetadataSetRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *MessageMetadataSetRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



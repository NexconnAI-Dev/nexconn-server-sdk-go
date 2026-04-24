# OpenChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. | 
**ToChannelIds** | **[]string** | Target open channel IDs. Multiple channels are allowed; the official documentation recommends up to 10 IDs per request. | 
**MessageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in open channel cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**IsEchoToSender** | Pointer to **int32** | Whether to sync the sent message to the sender&#39;s client while online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] 
**Priority** | Pointer to **int32** | Message priority. &#x60;0&#x60; standard, &#x60;1&#x60; allowlisted, &#x60;2&#x60; high priority, &#x60;3&#x60; low priority. | [optional] 

## Methods

### NewOpenChannelMessageSendRequest

`func NewOpenChannelMessageSendRequest(fromUserId string, toChannelIds []string, messageType string, content string, ) *OpenChannelMessageSendRequest`

NewOpenChannelMessageSendRequest instantiates a new OpenChannelMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMessageSendRequestWithDefaults

`func NewOpenChannelMessageSendRequestWithDefaults() *OpenChannelMessageSendRequest`

NewOpenChannelMessageSendRequestWithDefaults instantiates a new OpenChannelMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *OpenChannelMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *OpenChannelMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *OpenChannelMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToChannelIds

`func (o *OpenChannelMessageSendRequest) GetToChannelIds() []string`

GetToChannelIds returns the ToChannelIds field if non-nil, zero value otherwise.

### GetToChannelIdsOk

`func (o *OpenChannelMessageSendRequest) GetToChannelIdsOk() (*[]string, bool)`

GetToChannelIdsOk returns a tuple with the ToChannelIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToChannelIds

`func (o *OpenChannelMessageSendRequest) SetToChannelIds(v []string)`

SetToChannelIds sets ToChannelIds field to given value.


### GetMessageType

`func (o *OpenChannelMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *OpenChannelMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *OpenChannelMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *OpenChannelMessageSendRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *OpenChannelMessageSendRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *OpenChannelMessageSendRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetShouldPersist

`func (o *OpenChannelMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *OpenChannelMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *OpenChannelMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *OpenChannelMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetIsEchoToSender

`func (o *OpenChannelMessageSendRequest) GetIsEchoToSender() int32`

GetIsEchoToSender returns the IsEchoToSender field if non-nil, zero value otherwise.

### GetIsEchoToSenderOk

`func (o *OpenChannelMessageSendRequest) GetIsEchoToSenderOk() (*int32, bool)`

GetIsEchoToSenderOk returns a tuple with the IsEchoToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsEchoToSender

`func (o *OpenChannelMessageSendRequest) SetIsEchoToSender(v int32)`

SetIsEchoToSender sets IsEchoToSender field to given value.

### HasIsEchoToSender

`func (o *OpenChannelMessageSendRequest) HasIsEchoToSender() bool`

HasIsEchoToSender returns a boolean if a field has been set.

### GetPriority

`func (o *OpenChannelMessageSendRequest) GetPriority() int32`

GetPriority returns the Priority field if non-nil, zero value otherwise.

### GetPriorityOk

`func (o *OpenChannelMessageSendRequest) GetPriorityOk() (*int32, bool)`

GetPriorityOk returns a tuple with the Priority field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPriority

`func (o *OpenChannelMessageSendRequest) SetPriority(v int32)`

SetPriority sets Priority field to given value.

### HasPriority

`func (o *OpenChannelMessageSendRequest) HasPriority() bool`

HasPriority returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



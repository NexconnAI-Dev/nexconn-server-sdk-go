# ChannelTypeMessageMetadataDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**UserId** | **string** |  | 
**ChannelType** | **int32** | Supports direct and group channels. Legacy field name is &#x60;conversationType&#x60;. | 
**ChannelId** | **string** | Legacy &#x60;targetId&#x60;. | 
**Keys** | **[]string** |  | 
**SyncToSender** | Pointer to **int32** | Legacy &#x60;syncToSender&#x60;. &#x60;0&#x60; by default. | [optional] 

## Methods

### NewChannelTypeMessageMetadataDeleteRequest

`func NewChannelTypeMessageMetadataDeleteRequest(messageId string, userId string, channelType int32, channelId string, keys []string, ) *ChannelTypeMessageMetadataDeleteRequest`

NewChannelTypeMessageMetadataDeleteRequest instantiates a new ChannelTypeMessageMetadataDeleteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeMessageMetadataDeleteRequestWithDefaults

`func NewChannelTypeMessageMetadataDeleteRequestWithDefaults() *ChannelTypeMessageMetadataDeleteRequest`

NewChannelTypeMessageMetadataDeleteRequestWithDefaults instantiates a new ChannelTypeMessageMetadataDeleteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetUserId

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelType

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.


### GetChannelId

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetKeys

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetKeys() []string`

GetKeys returns the Keys field if non-nil, zero value otherwise.

### GetKeysOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetKeysOk() (*[]string, bool)`

GetKeysOk returns a tuple with the Keys field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKeys

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetKeys(v []string)`

SetKeys sets Keys field to given value.


### GetSyncToSender

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetSyncToSender() int32`

GetSyncToSender returns the SyncToSender field if non-nil, zero value otherwise.

### GetSyncToSenderOk

`func (o *ChannelTypeMessageMetadataDeleteRequest) GetSyncToSenderOk() (*int32, bool)`

GetSyncToSenderOk returns a tuple with the SyncToSender field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSyncToSender

`func (o *ChannelTypeMessageMetadataDeleteRequest) SetSyncToSender(v int32)`

SetSyncToSender sets SyncToSender field to given value.

### HasSyncToSender

`func (o *ChannelTypeMessageMetadataDeleteRequest) HasSyncToSender() bool`

HasSyncToSender returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



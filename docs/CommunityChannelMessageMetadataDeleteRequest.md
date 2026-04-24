# CommunityChannelMessageMetadataDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**UserId** | **string** |  | 
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** | Should match the subchannel used when the message was sent. | [optional] 
**Keys** | **[]string** |  | 

## Methods

### NewCommunityChannelMessageMetadataDeleteRequest

`func NewCommunityChannelMessageMetadataDeleteRequest(messageId string, userId string, channelId string, keys []string, ) *CommunityChannelMessageMetadataDeleteRequest`

NewCommunityChannelMessageMetadataDeleteRequest instantiates a new CommunityChannelMessageMetadataDeleteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageMetadataDeleteRequestWithDefaults

`func NewCommunityChannelMessageMetadataDeleteRequestWithDefaults() *CommunityChannelMessageMetadataDeleteRequest`

NewCommunityChannelMessageMetadataDeleteRequestWithDefaults instantiates a new CommunityChannelMessageMetadataDeleteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *CommunityChannelMessageMetadataDeleteRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetUserId

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityChannelMessageMetadataDeleteRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelId

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelMessageMetadataDeleteRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelMessageMetadataDeleteRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelMessageMetadataDeleteRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetKeys

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetKeys() []string`

GetKeys returns the Keys field if non-nil, zero value otherwise.

### GetKeysOk

`func (o *CommunityChannelMessageMetadataDeleteRequest) GetKeysOk() (*[]string, bool)`

GetKeysOk returns a tuple with the Keys field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKeys

`func (o *CommunityChannelMessageMetadataDeleteRequest) SetKeys(v []string)`

SetKeys sets Keys field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



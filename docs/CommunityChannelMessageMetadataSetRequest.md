# CommunityChannelMessageMetadataSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**UserId** | **string** |  | 
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**Metadata** | **map[string]string** | Community-channel message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 20 entries.  | 

## Methods

### NewCommunityChannelMessageMetadataSetRequest

`func NewCommunityChannelMessageMetadataSetRequest(messageId string, userId string, channelId string, metadata map[string]string, ) *CommunityChannelMessageMetadataSetRequest`

NewCommunityChannelMessageMetadataSetRequest instantiates a new CommunityChannelMessageMetadataSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageMetadataSetRequestWithDefaults

`func NewCommunityChannelMessageMetadataSetRequestWithDefaults() *CommunityChannelMessageMetadataSetRequest`

NewCommunityChannelMessageMetadataSetRequestWithDefaults instantiates a new CommunityChannelMessageMetadataSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *CommunityChannelMessageMetadataSetRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *CommunityChannelMessageMetadataSetRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *CommunityChannelMessageMetadataSetRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetUserId

`func (o *CommunityChannelMessageMetadataSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityChannelMessageMetadataSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityChannelMessageMetadataSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelId

`func (o *CommunityChannelMessageMetadataSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelMessageMetadataSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelMessageMetadataSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelMessageMetadataSetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelMessageMetadataSetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelMessageMetadataSetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelMessageMetadataSetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetMetadata

`func (o *CommunityChannelMessageMetadataSetRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *CommunityChannelMessageMetadataSetRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *CommunityChannelMessageMetadataSetRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# CommunityChannelMessageUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**FromUserId** | **string** |  | 
**MessageId** | **string** |  | 
**Content** | **string** |  | 

## Methods

### NewCommunityChannelMessageUpdateRequest

`func NewCommunityChannelMessageUpdateRequest(channelId string, fromUserId string, messageId string, content string, ) *CommunityChannelMessageUpdateRequest`

NewCommunityChannelMessageUpdateRequest instantiates a new CommunityChannelMessageUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageUpdateRequestWithDefaults

`func NewCommunityChannelMessageUpdateRequestWithDefaults() *CommunityChannelMessageUpdateRequest`

NewCommunityChannelMessageUpdateRequestWithDefaults instantiates a new CommunityChannelMessageUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelMessageUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelMessageUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelMessageUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelMessageUpdateRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelMessageUpdateRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelMessageUpdateRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelMessageUpdateRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetFromUserId

`func (o *CommunityChannelMessageUpdateRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *CommunityChannelMessageUpdateRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *CommunityChannelMessageUpdateRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetMessageId

`func (o *CommunityChannelMessageUpdateRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *CommunityChannelMessageUpdateRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *CommunityChannelMessageUpdateRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetContent

`func (o *CommunityChannelMessageUpdateRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *CommunityChannelMessageUpdateRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *CommunityChannelMessageUpdateRequest) SetContent(v string)`

SetContent sets Content field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



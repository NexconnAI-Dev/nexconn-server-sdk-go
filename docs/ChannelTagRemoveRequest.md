# ChannelTagRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TagId** | **string** |  | 
**Channels** | [**[]ChannelTagTargetItem**](ChannelTagTargetItem.md) |  | 

## Methods

### NewChannelTagRemoveRequest

`func NewChannelTagRemoveRequest(userId string, tagId string, channels []ChannelTagTargetItem, ) *ChannelTagRemoveRequest`

NewChannelTagRemoveRequest instantiates a new ChannelTagRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTagRemoveRequestWithDefaults

`func NewChannelTagRemoveRequestWithDefaults() *ChannelTagRemoveRequest`

NewChannelTagRemoveRequestWithDefaults instantiates a new ChannelTagRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *ChannelTagRemoveRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *ChannelTagRemoveRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *ChannelTagRemoveRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTagId

`func (o *ChannelTagRemoveRequest) GetTagId() string`

GetTagId returns the TagId field if non-nil, zero value otherwise.

### GetTagIdOk

`func (o *ChannelTagRemoveRequest) GetTagIdOk() (*string, bool)`

GetTagIdOk returns a tuple with the TagId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTagId

`func (o *ChannelTagRemoveRequest) SetTagId(v string)`

SetTagId sets TagId field to given value.


### GetChannels

`func (o *ChannelTagRemoveRequest) GetChannels() []ChannelTagTargetItem`

GetChannels returns the Channels field if non-nil, zero value otherwise.

### GetChannelsOk

`func (o *ChannelTagRemoveRequest) GetChannelsOk() (*[]ChannelTagTargetItem, bool)`

GetChannelsOk returns a tuple with the Channels field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannels

`func (o *ChannelTagRemoveRequest) SetChannels(v []ChannelTagTargetItem)`

SetChannels sets Channels field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



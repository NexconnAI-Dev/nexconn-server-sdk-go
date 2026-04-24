# ChannelTagListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TagId** | Pointer to **string** |  | [optional] 
**Channels** | Pointer to [**[]ChannelTagTargetItem**](ChannelTagTargetItem.md) |  | [optional] 

## Methods

### NewChannelTagListResponseResult

`func NewChannelTagListResponseResult() *ChannelTagListResponseResult`

NewChannelTagListResponseResult instantiates a new ChannelTagListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTagListResponseResultWithDefaults

`func NewChannelTagListResponseResultWithDefaults() *ChannelTagListResponseResult`

NewChannelTagListResponseResultWithDefaults instantiates a new ChannelTagListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTagId

`func (o *ChannelTagListResponseResult) GetTagId() string`

GetTagId returns the TagId field if non-nil, zero value otherwise.

### GetTagIdOk

`func (o *ChannelTagListResponseResult) GetTagIdOk() (*string, bool)`

GetTagIdOk returns a tuple with the TagId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTagId

`func (o *ChannelTagListResponseResult) SetTagId(v string)`

SetTagId sets TagId field to given value.

### HasTagId

`func (o *ChannelTagListResponseResult) HasTagId() bool`

HasTagId returns a boolean if a field has been set.

### GetChannels

`func (o *ChannelTagListResponseResult) GetChannels() []ChannelTagTargetItem`

GetChannels returns the Channels field if non-nil, zero value otherwise.

### GetChannelsOk

`func (o *ChannelTagListResponseResult) GetChannelsOk() (*[]ChannelTagTargetItem, bool)`

GetChannelsOk returns a tuple with the Channels field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannels

`func (o *ChannelTagListResponseResult) SetChannels(v []ChannelTagTargetItem)`

SetChannels sets Channels field to given value.

### HasChannels

`func (o *ChannelTagListResponseResult) HasChannels() bool`

HasChannels returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ChannelPinState

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsPinned** | Pointer to **bool** |  | [optional] 
**PinnedAt** | Pointer to **int64** |  | [optional] 

## Methods

### NewChannelPinState

`func NewChannelPinState() *ChannelPinState`

NewChannelPinState instantiates a new ChannelPinState object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelPinStateWithDefaults

`func NewChannelPinStateWithDefaults() *ChannelPinState`

NewChannelPinStateWithDefaults instantiates a new ChannelPinState object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetIsPinned

`func (o *ChannelPinState) GetIsPinned() bool`

GetIsPinned returns the IsPinned field if non-nil, zero value otherwise.

### GetIsPinnedOk

`func (o *ChannelPinState) GetIsPinnedOk() (*bool, bool)`

GetIsPinnedOk returns a tuple with the IsPinned field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsPinned

`func (o *ChannelPinState) SetIsPinned(v bool)`

SetIsPinned sets IsPinned field to given value.

### HasIsPinned

`func (o *ChannelPinState) HasIsPinned() bool`

HasIsPinned returns a boolean if a field has been set.

### GetPinnedAt

`func (o *ChannelPinState) GetPinnedAt() int64`

GetPinnedAt returns the PinnedAt field if non-nil, zero value otherwise.

### GetPinnedAtOk

`func (o *ChannelPinState) GetPinnedAtOk() (*int64, bool)`

GetPinnedAtOk returns a tuple with the PinnedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPinnedAt

`func (o *ChannelPinState) SetPinnedAt(v int64)`

SetPinnedAt sets PinnedAt field to given value.

### HasPinnedAt

`func (o *ChannelPinState) HasPinnedAt() bool`

HasPinnedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



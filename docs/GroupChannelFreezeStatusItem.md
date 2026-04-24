# GroupChannelFreezeStatusItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** |  | [optional] 
**Status** | Pointer to **int32** | Freeze status defined by the source API. | [optional] 

## Methods

### NewGroupChannelFreezeStatusItem

`func NewGroupChannelFreezeStatusItem() *GroupChannelFreezeStatusItem`

NewGroupChannelFreezeStatusItem instantiates a new GroupChannelFreezeStatusItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelFreezeStatusItemWithDefaults

`func NewGroupChannelFreezeStatusItemWithDefaults() *GroupChannelFreezeStatusItem`

NewGroupChannelFreezeStatusItemWithDefaults instantiates a new GroupChannelFreezeStatusItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelFreezeStatusItem) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelFreezeStatusItem) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelFreezeStatusItem) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelFreezeStatusItem) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetStatus

`func (o *GroupChannelFreezeStatusItem) GetStatus() int32`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *GroupChannelFreezeStatusItem) GetStatusOk() (*int32, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *GroupChannelFreezeStatusItem) SetStatus(v int32)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *GroupChannelFreezeStatusItem) HasStatus() bool`

HasStatus returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# GroupChannelFreezeListGetResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FreezeStatuses** | Pointer to [**[]GroupChannelFreezeStatusItem**](GroupChannelFreezeStatusItem.md) |  | [optional] 

## Methods

### NewGroupChannelFreezeListGetResponseResult

`func NewGroupChannelFreezeListGetResponseResult() *GroupChannelFreezeListGetResponseResult`

NewGroupChannelFreezeListGetResponseResult instantiates a new GroupChannelFreezeListGetResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelFreezeListGetResponseResultWithDefaults

`func NewGroupChannelFreezeListGetResponseResultWithDefaults() *GroupChannelFreezeListGetResponseResult`

NewGroupChannelFreezeListGetResponseResultWithDefaults instantiates a new GroupChannelFreezeListGetResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFreezeStatuses

`func (o *GroupChannelFreezeListGetResponseResult) GetFreezeStatuses() []GroupChannelFreezeStatusItem`

GetFreezeStatuses returns the FreezeStatuses field if non-nil, zero value otherwise.

### GetFreezeStatusesOk

`func (o *GroupChannelFreezeListGetResponseResult) GetFreezeStatusesOk() (*[]GroupChannelFreezeStatusItem, bool)`

GetFreezeStatusesOk returns a tuple with the FreezeStatuses field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFreezeStatuses

`func (o *GroupChannelFreezeListGetResponseResult) SetFreezeStatuses(v []GroupChannelFreezeStatusItem)`

SetFreezeStatuses sets FreezeStatuses field to given value.

### HasFreezeStatuses

`func (o *GroupChannelFreezeListGetResponseResult) HasFreezeStatuses() bool`

HasFreezeStatuses returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



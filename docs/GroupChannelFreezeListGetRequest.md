# GroupChannelFreezeListGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelIds** | Pointer to **[]string** | Optional specific group channel IDs to query. | [optional] 
**Page** | Pointer to **int32** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] 

## Methods

### NewGroupChannelFreezeListGetRequest

`func NewGroupChannelFreezeListGetRequest() *GroupChannelFreezeListGetRequest`

NewGroupChannelFreezeListGetRequest instantiates a new GroupChannelFreezeListGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelFreezeListGetRequestWithDefaults

`func NewGroupChannelFreezeListGetRequestWithDefaults() *GroupChannelFreezeListGetRequest`

NewGroupChannelFreezeListGetRequestWithDefaults instantiates a new GroupChannelFreezeListGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelIds

`func (o *GroupChannelFreezeListGetRequest) GetChannelIds() []string`

GetChannelIds returns the ChannelIds field if non-nil, zero value otherwise.

### GetChannelIdsOk

`func (o *GroupChannelFreezeListGetRequest) GetChannelIdsOk() (*[]string, bool)`

GetChannelIdsOk returns a tuple with the ChannelIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelIds

`func (o *GroupChannelFreezeListGetRequest) SetChannelIds(v []string)`

SetChannelIds sets ChannelIds field to given value.

### HasChannelIds

`func (o *GroupChannelFreezeListGetRequest) HasChannelIds() bool`

HasChannelIds returns a boolean if a field has been set.

### GetPage

`func (o *GroupChannelFreezeListGetRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *GroupChannelFreezeListGetRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *GroupChannelFreezeListGetRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *GroupChannelFreezeListGetRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *GroupChannelFreezeListGetRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *GroupChannelFreezeListGetRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *GroupChannelFreezeListGetRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *GroupChannelFreezeListGetRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



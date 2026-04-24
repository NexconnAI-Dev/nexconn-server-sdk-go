# GroupChannelListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] 
**Order** | Pointer to **int32** |  | [optional] 

## Methods

### NewGroupChannelListRequest

`func NewGroupChannelListRequest() *GroupChannelListRequest`

NewGroupChannelListRequest instantiates a new GroupChannelListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelListRequestWithDefaults

`func NewGroupChannelListRequestWithDefaults() *GroupChannelListRequest`

NewGroupChannelListRequestWithDefaults instantiates a new GroupChannelListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *GroupChannelListRequest) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelListRequest) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelListRequest) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelListRequest) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetPageSize

`func (o *GroupChannelListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *GroupChannelListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *GroupChannelListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *GroupChannelListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *GroupChannelListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *GroupChannelListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *GroupChannelListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *GroupChannelListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



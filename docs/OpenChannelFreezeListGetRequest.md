# OpenChannelFreezeListGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Page** | Pointer to **int32** |  | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 50]

## Methods

### NewOpenChannelFreezeListGetRequest

`func NewOpenChannelFreezeListGetRequest() *OpenChannelFreezeListGetRequest`

NewOpenChannelFreezeListGetRequest instantiates a new OpenChannelFreezeListGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelFreezeListGetRequestWithDefaults

`func NewOpenChannelFreezeListGetRequestWithDefaults() *OpenChannelFreezeListGetRequest`

NewOpenChannelFreezeListGetRequestWithDefaults instantiates a new OpenChannelFreezeListGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPage

`func (o *OpenChannelFreezeListGetRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *OpenChannelFreezeListGetRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *OpenChannelFreezeListGetRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *OpenChannelFreezeListGetRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *OpenChannelFreezeListGetRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *OpenChannelFreezeListGetRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *OpenChannelFreezeListGetRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *OpenChannelFreezeListGetRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



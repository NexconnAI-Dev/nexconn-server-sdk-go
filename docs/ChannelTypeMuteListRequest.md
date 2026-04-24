# ChannelTypeMuteListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageSize** | Pointer to **int32** |  | [optional] [default to 100]
**Offset** | Pointer to **int32** |  | [optional] [default to 0]
**ChannelType** | **string** |  | 

## Methods

### NewChannelTypeMuteListRequest

`func NewChannelTypeMuteListRequest(channelType string, ) *ChannelTypeMuteListRequest`

NewChannelTypeMuteListRequest instantiates a new ChannelTypeMuteListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeMuteListRequestWithDefaults

`func NewChannelTypeMuteListRequestWithDefaults() *ChannelTypeMuteListRequest`

NewChannelTypeMuteListRequestWithDefaults instantiates a new ChannelTypeMuteListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageSize

`func (o *ChannelTypeMuteListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *ChannelTypeMuteListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *ChannelTypeMuteListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *ChannelTypeMuteListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOffset

`func (o *ChannelTypeMuteListRequest) GetOffset() int32`

GetOffset returns the Offset field if non-nil, zero value otherwise.

### GetOffsetOk

`func (o *ChannelTypeMuteListRequest) GetOffsetOk() (*int32, bool)`

GetOffsetOk returns a tuple with the Offset field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOffset

`func (o *ChannelTypeMuteListRequest) SetOffset(v int32)`

SetOffset sets Offset field to given value.

### HasOffset

`func (o *ChannelTypeMuteListRequest) HasOffset() bool`

HasOffset returns a boolean if a field has been set.

### GetChannelType

`func (o *ChannelTypeMuteListRequest) GetChannelType() string`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelTypeMuteListRequest) GetChannelTypeOk() (*string, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelTypeMuteListRequest) SetChannelType(v string)`

SetChannelType sets ChannelType field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



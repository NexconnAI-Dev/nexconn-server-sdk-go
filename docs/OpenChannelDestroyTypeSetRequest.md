# OpenChannelDestroyTypeSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**DestroyType** | Pointer to **int32** |  | [optional] 
**TtlMinutes** | Pointer to **int32** |  | [optional] 

## Methods

### NewOpenChannelDestroyTypeSetRequest

`func NewOpenChannelDestroyTypeSetRequest(channelId string, ) *OpenChannelDestroyTypeSetRequest`

NewOpenChannelDestroyTypeSetRequest instantiates a new OpenChannelDestroyTypeSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelDestroyTypeSetRequestWithDefaults

`func NewOpenChannelDestroyTypeSetRequestWithDefaults() *OpenChannelDestroyTypeSetRequest`

NewOpenChannelDestroyTypeSetRequestWithDefaults instantiates a new OpenChannelDestroyTypeSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelDestroyTypeSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelDestroyTypeSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelDestroyTypeSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetDestroyType

`func (o *OpenChannelDestroyTypeSetRequest) GetDestroyType() int32`

GetDestroyType returns the DestroyType field if non-nil, zero value otherwise.

### GetDestroyTypeOk

`func (o *OpenChannelDestroyTypeSetRequest) GetDestroyTypeOk() (*int32, bool)`

GetDestroyTypeOk returns a tuple with the DestroyType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDestroyType

`func (o *OpenChannelDestroyTypeSetRequest) SetDestroyType(v int32)`

SetDestroyType sets DestroyType field to given value.

### HasDestroyType

`func (o *OpenChannelDestroyTypeSetRequest) HasDestroyType() bool`

HasDestroyType returns a boolean if a field has been set.

### GetTtlMinutes

`func (o *OpenChannelDestroyTypeSetRequest) GetTtlMinutes() int32`

GetTtlMinutes returns the TtlMinutes field if non-nil, zero value otherwise.

### GetTtlMinutesOk

`func (o *OpenChannelDestroyTypeSetRequest) GetTtlMinutesOk() (*int32, bool)`

GetTtlMinutesOk returns a tuple with the TtlMinutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlMinutes

`func (o *OpenChannelDestroyTypeSetRequest) SetTtlMinutes(v int32)`

SetTtlMinutes sets TtlMinutes field to given value.

### HasTtlMinutes

`func (o *OpenChannelDestroyTypeSetRequest) HasTtlMinutes() bool`

HasTtlMinutes returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



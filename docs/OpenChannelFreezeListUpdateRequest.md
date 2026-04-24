# OpenChannelFreezeListUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**Extra** | Pointer to **string** | Notification extra payload in JSON string format. | [optional] 
**NeedNotify** | Pointer to **bool** |  | [optional] 

## Methods

### NewOpenChannelFreezeListUpdateRequest

`func NewOpenChannelFreezeListUpdateRequest(channelId string, ) *OpenChannelFreezeListUpdateRequest`

NewOpenChannelFreezeListUpdateRequest instantiates a new OpenChannelFreezeListUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelFreezeListUpdateRequestWithDefaults

`func NewOpenChannelFreezeListUpdateRequestWithDefaults() *OpenChannelFreezeListUpdateRequest`

NewOpenChannelFreezeListUpdateRequestWithDefaults instantiates a new OpenChannelFreezeListUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelFreezeListUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelFreezeListUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelFreezeListUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetExtra

`func (o *OpenChannelFreezeListUpdateRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *OpenChannelFreezeListUpdateRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *OpenChannelFreezeListUpdateRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *OpenChannelFreezeListUpdateRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetNeedNotify

`func (o *OpenChannelFreezeListUpdateRequest) GetNeedNotify() bool`

GetNeedNotify returns the NeedNotify field if non-nil, zero value otherwise.

### GetNeedNotifyOk

`func (o *OpenChannelFreezeListUpdateRequest) GetNeedNotifyOk() (*bool, bool)`

GetNeedNotifyOk returns a tuple with the NeedNotify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedNotify

`func (o *OpenChannelFreezeListUpdateRequest) SetNeedNotify(v bool)`

SetNeedNotify sets NeedNotify field to given value.

### HasNeedNotify

`func (o *OpenChannelFreezeListUpdateRequest) HasNeedNotify() bool`

HasNeedNotify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



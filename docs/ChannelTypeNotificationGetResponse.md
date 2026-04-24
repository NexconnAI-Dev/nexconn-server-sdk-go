# ChannelTypeNotificationGetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**ChannelTypeNotificationGetResponseResult**](ChannelTypeNotificationGetResponseResult.md) |  | [optional] 

## Methods

### NewChannelTypeNotificationGetResponse

`func NewChannelTypeNotificationGetResponse(code int32, ) *ChannelTypeNotificationGetResponse`

NewChannelTypeNotificationGetResponse instantiates a new ChannelTypeNotificationGetResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeNotificationGetResponseWithDefaults

`func NewChannelTypeNotificationGetResponseWithDefaults() *ChannelTypeNotificationGetResponse`

NewChannelTypeNotificationGetResponseWithDefaults instantiates a new ChannelTypeNotificationGetResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *ChannelTypeNotificationGetResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *ChannelTypeNotificationGetResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *ChannelTypeNotificationGetResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *ChannelTypeNotificationGetResponse) GetResult() ChannelTypeNotificationGetResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *ChannelTypeNotificationGetResponse) GetResultOk() (*ChannelTypeNotificationGetResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *ChannelTypeNotificationGetResponse) SetResult(v ChannelTypeNotificationGetResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *ChannelTypeNotificationGetResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# SystemChannelPushResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**SystemChannelPushResponseResult**](SystemChannelPushResponseResult.md) |  | [optional] 

## Methods

### NewSystemChannelPushResponse

`func NewSystemChannelPushResponse(code int32, ) *SystemChannelPushResponse`

NewSystemChannelPushResponse instantiates a new SystemChannelPushResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelPushResponseWithDefaults

`func NewSystemChannelPushResponseWithDefaults() *SystemChannelPushResponse`

NewSystemChannelPushResponseWithDefaults instantiates a new SystemChannelPushResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *SystemChannelPushResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *SystemChannelPushResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *SystemChannelPushResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *SystemChannelPushResponse) GetResult() SystemChannelPushResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *SystemChannelPushResponse) GetResultOk() (*SystemChannelPushResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *SystemChannelPushResponse) SetResult(v SystemChannelPushResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *SystemChannelPushResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



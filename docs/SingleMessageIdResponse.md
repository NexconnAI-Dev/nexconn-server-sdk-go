# SingleMessageIdResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**SingleMessageIdResponseResult**](SingleMessageIdResponseResult.md) |  | [optional] 

## Methods

### NewSingleMessageIdResponse

`func NewSingleMessageIdResponse(code int32, ) *SingleMessageIdResponse`

NewSingleMessageIdResponse instantiates a new SingleMessageIdResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSingleMessageIdResponseWithDefaults

`func NewSingleMessageIdResponseWithDefaults() *SingleMessageIdResponse`

NewSingleMessageIdResponseWithDefaults instantiates a new SingleMessageIdResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *SingleMessageIdResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *SingleMessageIdResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *SingleMessageIdResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *SingleMessageIdResponse) GetResult() SingleMessageIdResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *SingleMessageIdResponse) GetResultOk() (*SingleMessageIdResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *SingleMessageIdResponse) SetResult(v SingleMessageIdResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *SingleMessageIdResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



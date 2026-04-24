# UserOperationResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**UserOperationResponseResult**](UserOperationResponseResult.md) |  | [optional] 

## Methods

### NewUserOperationResponse

`func NewUserOperationResponse(code int32, ) *UserOperationResponse`

NewUserOperationResponse instantiates a new UserOperationResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserOperationResponseWithDefaults

`func NewUserOperationResponseWithDefaults() *UserOperationResponse`

NewUserOperationResponseWithDefaults instantiates a new UserOperationResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *UserOperationResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *UserOperationResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *UserOperationResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *UserOperationResponse) GetResult() UserOperationResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *UserOperationResponse) GetResultOk() (*UserOperationResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *UserOperationResponse) SetResult(v UserOperationResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *UserOperationResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# UserConnectionStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**UserConnectionStatusResponseResult**](UserConnectionStatusResponseResult.md) |  | [optional] 

## Methods

### NewUserConnectionStatusResponse

`func NewUserConnectionStatusResponse(code int32, ) *UserConnectionStatusResponse`

NewUserConnectionStatusResponse instantiates a new UserConnectionStatusResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserConnectionStatusResponseWithDefaults

`func NewUserConnectionStatusResponseWithDefaults() *UserConnectionStatusResponse`

NewUserConnectionStatusResponseWithDefaults instantiates a new UserConnectionStatusResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *UserConnectionStatusResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *UserConnectionStatusResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *UserConnectionStatusResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *UserConnectionStatusResponse) GetResult() UserConnectionStatusResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *UserConnectionStatusResponse) GetResultOk() (*UserConnectionStatusResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *UserConnectionStatusResponse) SetResult(v UserConnectionStatusResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *UserConnectionStatusResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



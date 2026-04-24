# UserSoftDeletedListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**UserSoftDeletedListResponseResult**](UserSoftDeletedListResponseResult.md) |  | [optional] 

## Methods

### NewUserSoftDeletedListResponse

`func NewUserSoftDeletedListResponse(code int32, ) *UserSoftDeletedListResponse`

NewUserSoftDeletedListResponse instantiates a new UserSoftDeletedListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserSoftDeletedListResponseWithDefaults

`func NewUserSoftDeletedListResponseWithDefaults() *UserSoftDeletedListResponse`

NewUserSoftDeletedListResponseWithDefaults instantiates a new UserSoftDeletedListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *UserSoftDeletedListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *UserSoftDeletedListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *UserSoftDeletedListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *UserSoftDeletedListResponse) GetResult() UserSoftDeletedListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *UserSoftDeletedListResponse) GetResultOk() (*UserSoftDeletedListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *UserSoftDeletedListResponse) SetResult(v UserSoftDeletedListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *UserSoftDeletedListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



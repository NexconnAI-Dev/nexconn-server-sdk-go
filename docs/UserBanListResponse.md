# UserBanListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**UserBanListResponseResult**](UserBanListResponseResult.md) |  | [optional] 

## Methods

### NewUserBanListResponse

`func NewUserBanListResponse(code int32, ) *UserBanListResponse`

NewUserBanListResponse instantiates a new UserBanListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBanListResponseWithDefaults

`func NewUserBanListResponseWithDefaults() *UserBanListResponse`

NewUserBanListResponseWithDefaults instantiates a new UserBanListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *UserBanListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *UserBanListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *UserBanListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *UserBanListResponse) GetResult() UserBanListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *UserBanListResponse) GetResultOk() (*UserBanListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *UserBanListResponse) SetResult(v UserBanListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *UserBanListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



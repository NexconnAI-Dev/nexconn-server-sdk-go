# FriendListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**FriendListResponseResult**](FriendListResponseResult.md) |  | [optional] 

## Methods

### NewFriendListResponse

`func NewFriendListResponse(code int32, ) *FriendListResponse`

NewFriendListResponse instantiates a new FriendListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendListResponseWithDefaults

`func NewFriendListResponseWithDefaults() *FriendListResponse`

NewFriendListResponseWithDefaults instantiates a new FriendListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *FriendListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *FriendListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *FriendListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *FriendListResponse) GetResult() FriendListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *FriendListResponse) GetResultOk() (*FriendListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *FriendListResponse) SetResult(v FriendListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *FriendListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FriendRelationshipGetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**FriendRelationshipGetResponseResult**](FriendRelationshipGetResponseResult.md) |  | [optional] 

## Methods

### NewFriendRelationshipGetResponse

`func NewFriendRelationshipGetResponse(code int32, ) *FriendRelationshipGetResponse`

NewFriendRelationshipGetResponse instantiates a new FriendRelationshipGetResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendRelationshipGetResponseWithDefaults

`func NewFriendRelationshipGetResponseWithDefaults() *FriendRelationshipGetResponse`

NewFriendRelationshipGetResponseWithDefaults instantiates a new FriendRelationshipGetResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *FriendRelationshipGetResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *FriendRelationshipGetResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *FriendRelationshipGetResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *FriendRelationshipGetResponse) GetResult() FriendRelationshipGetResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *FriendRelationshipGetResponse) GetResultOk() (*FriendRelationshipGetResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *FriendRelationshipGetResponse) SetResult(v FriendRelationshipGetResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *FriendRelationshipGetResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



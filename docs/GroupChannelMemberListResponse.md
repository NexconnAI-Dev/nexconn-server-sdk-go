# GroupChannelMemberListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**GroupChannelMemberListResponseResult**](GroupChannelMemberListResponseResult.md) |  | [optional] 

## Methods

### NewGroupChannelMemberListResponse

`func NewGroupChannelMemberListResponse(code int32, ) *GroupChannelMemberListResponse`

NewGroupChannelMemberListResponse instantiates a new GroupChannelMemberListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberListResponseWithDefaults

`func NewGroupChannelMemberListResponseWithDefaults() *GroupChannelMemberListResponse`

NewGroupChannelMemberListResponseWithDefaults instantiates a new GroupChannelMemberListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *GroupChannelMemberListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *GroupChannelMemberListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *GroupChannelMemberListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *GroupChannelMemberListResponse) GetResult() GroupChannelMemberListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *GroupChannelMemberListResponse) GetResultOk() (*GroupChannelMemberListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *GroupChannelMemberListResponse) SetResult(v GroupChannelMemberListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *GroupChannelMemberListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



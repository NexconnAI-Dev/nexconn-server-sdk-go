# CommunityPrivateSubchannelMemberListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**CommunityPrivateSubchannelMemberListResponseResult**](CommunityPrivateSubchannelMemberListResponseResult.md) |  | [optional] 

## Methods

### NewCommunityPrivateSubchannelMemberListResponse

`func NewCommunityPrivateSubchannelMemberListResponse(code int32, ) *CommunityPrivateSubchannelMemberListResponse`

NewCommunityPrivateSubchannelMemberListResponse instantiates a new CommunityPrivateSubchannelMemberListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityPrivateSubchannelMemberListResponseWithDefaults

`func NewCommunityPrivateSubchannelMemberListResponseWithDefaults() *CommunityPrivateSubchannelMemberListResponse`

NewCommunityPrivateSubchannelMemberListResponseWithDefaults instantiates a new CommunityPrivateSubchannelMemberListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *CommunityPrivateSubchannelMemberListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *CommunityPrivateSubchannelMemberListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *CommunityPrivateSubchannelMemberListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *CommunityPrivateSubchannelMemberListResponse) GetResult() CommunityPrivateSubchannelMemberListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *CommunityPrivateSubchannelMemberListResponse) GetResultOk() (*CommunityPrivateSubchannelMemberListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *CommunityPrivateSubchannelMemberListResponse) SetResult(v CommunityPrivateSubchannelMemberListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *CommunityPrivateSubchannelMemberListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



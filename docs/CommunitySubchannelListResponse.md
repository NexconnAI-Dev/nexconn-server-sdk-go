# CommunitySubchannelListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**CommunitySubchannelListResponseResult**](CommunitySubchannelListResponseResult.md) |  | [optional] 

## Methods

### NewCommunitySubchannelListResponse

`func NewCommunitySubchannelListResponse(code int32, ) *CommunitySubchannelListResponse`

NewCommunitySubchannelListResponse instantiates a new CommunitySubchannelListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunitySubchannelListResponseWithDefaults

`func NewCommunitySubchannelListResponseWithDefaults() *CommunitySubchannelListResponse`

NewCommunitySubchannelListResponseWithDefaults instantiates a new CommunitySubchannelListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *CommunitySubchannelListResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *CommunitySubchannelListResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *CommunitySubchannelListResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *CommunitySubchannelListResponse) GetResult() CommunitySubchannelListResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *CommunitySubchannelListResponse) GetResultOk() (*CommunitySubchannelListResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *CommunitySubchannelListResponse) SetResult(v CommunitySubchannelListResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *CommunitySubchannelListResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



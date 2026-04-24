# AccessTokenIssueResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**AccessTokenIssueResult**](AccessTokenIssueResult.md) |  | [optional] 

## Methods

### NewAccessTokenIssueResponse

`func NewAccessTokenIssueResponse(code int32, ) *AccessTokenIssueResponse`

NewAccessTokenIssueResponse instantiates a new AccessTokenIssueResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAccessTokenIssueResponseWithDefaults

`func NewAccessTokenIssueResponseWithDefaults() *AccessTokenIssueResponse`

NewAccessTokenIssueResponseWithDefaults instantiates a new AccessTokenIssueResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *AccessTokenIssueResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *AccessTokenIssueResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *AccessTokenIssueResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *AccessTokenIssueResponse) GetResult() AccessTokenIssueResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *AccessTokenIssueResponse) GetResultOk() (*AccessTokenIssueResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *AccessTokenIssueResponse) SetResult(v AccessTokenIssueResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *AccessTokenIssueResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



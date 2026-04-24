# GroupChannelAllowedSenderListGetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**GroupChannelAllowedSenderListGetResponseResult**](GroupChannelAllowedSenderListGetResponseResult.md) |  | [optional] 

## Methods

### NewGroupChannelAllowedSenderListGetResponse

`func NewGroupChannelAllowedSenderListGetResponse(code int32, ) *GroupChannelAllowedSenderListGetResponse`

NewGroupChannelAllowedSenderListGetResponse instantiates a new GroupChannelAllowedSenderListGetResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelAllowedSenderListGetResponseWithDefaults

`func NewGroupChannelAllowedSenderListGetResponseWithDefaults() *GroupChannelAllowedSenderListGetResponse`

NewGroupChannelAllowedSenderListGetResponseWithDefaults instantiates a new GroupChannelAllowedSenderListGetResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *GroupChannelAllowedSenderListGetResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *GroupChannelAllowedSenderListGetResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *GroupChannelAllowedSenderListGetResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *GroupChannelAllowedSenderListGetResponse) GetResult() GroupChannelAllowedSenderListGetResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *GroupChannelAllowedSenderListGetResponse) GetResultOk() (*GroupChannelAllowedSenderListGetResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *GroupChannelAllowedSenderListGetResponse) SetResult(v GroupChannelAllowedSenderListGetResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *GroupChannelAllowedSenderListGetResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# OpenChannelParticipantExistResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** | Return code. &#x60;0&#x60; indicates success. | 
**Result** | Pointer to [**OpenChannelParticipantExistResponseResult**](OpenChannelParticipantExistResponseResult.md) |  | [optional] 

## Methods

### NewOpenChannelParticipantExistResponse

`func NewOpenChannelParticipantExistResponse(code int32, ) *OpenChannelParticipantExistResponse`

NewOpenChannelParticipantExistResponse instantiates a new OpenChannelParticipantExistResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantExistResponseWithDefaults

`func NewOpenChannelParticipantExistResponseWithDefaults() *OpenChannelParticipantExistResponse`

NewOpenChannelParticipantExistResponseWithDefaults instantiates a new OpenChannelParticipantExistResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *OpenChannelParticipantExistResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *OpenChannelParticipantExistResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *OpenChannelParticipantExistResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *OpenChannelParticipantExistResponse) GetResult() OpenChannelParticipantExistResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *OpenChannelParticipantExistResponse) GetResultOk() (*OpenChannelParticipantExistResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *OpenChannelParticipantExistResponse) SetResult(v OpenChannelParticipantExistResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *OpenChannelParticipantExistResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ChannelMessageSendResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**ChannelMessageSendResponseResult**](ChannelMessageSendResponseResult.md) |  | [optional] 

## Methods

### NewChannelMessageSendResponse

`func NewChannelMessageSendResponse(code int32, ) *ChannelMessageSendResponse`

NewChannelMessageSendResponse instantiates a new ChannelMessageSendResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelMessageSendResponseWithDefaults

`func NewChannelMessageSendResponseWithDefaults() *ChannelMessageSendResponse`

NewChannelMessageSendResponseWithDefaults instantiates a new ChannelMessageSendResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *ChannelMessageSendResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *ChannelMessageSendResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *ChannelMessageSendResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *ChannelMessageSendResponse) GetResult() ChannelMessageSendResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *ChannelMessageSendResponse) GetResultOk() (*ChannelMessageSendResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *ChannelMessageSendResponse) SetResult(v ChannelMessageSendResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *ChannelMessageSendResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



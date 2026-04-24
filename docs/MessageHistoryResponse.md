# MessageHistoryResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**Result** | Pointer to [**MessageHistoryResponseResult**](MessageHistoryResponseResult.md) |  | [optional] 

## Methods

### NewMessageHistoryResponse

`func NewMessageHistoryResponse(code int32, ) *MessageHistoryResponse`

NewMessageHistoryResponse instantiates a new MessageHistoryResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMessageHistoryResponseWithDefaults

`func NewMessageHistoryResponseWithDefaults() *MessageHistoryResponse`

NewMessageHistoryResponseWithDefaults instantiates a new MessageHistoryResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *MessageHistoryResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *MessageHistoryResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *MessageHistoryResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetResult

`func (o *MessageHistoryResponse) GetResult() MessageHistoryResponseResult`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *MessageHistoryResponse) GetResultOk() (*MessageHistoryResponseResult, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *MessageHistoryResponse) SetResult(v MessageHistoryResponseResult)`

SetResult sets Result field to given value.

### HasResult

`func (o *MessageHistoryResponse) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



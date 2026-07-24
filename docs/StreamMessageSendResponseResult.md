# StreamMessageSendResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | Pointer to **string** | Stream message unique ID. Only present in the response to the first chunk. | [optional] 

## Methods

### NewStreamMessageSendResponseResult

`func NewStreamMessageSendResponseResult() *StreamMessageSendResponseResult`

NewStreamMessageSendResponseResult instantiates a new StreamMessageSendResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewStreamMessageSendResponseResultWithDefaults

`func NewStreamMessageSendResponseResultWithDefaults() *StreamMessageSendResponseResult`

NewStreamMessageSendResponseResultWithDefaults instantiates a new StreamMessageSendResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *StreamMessageSendResponseResult) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *StreamMessageSendResponseResult) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *StreamMessageSendResponseResult) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.

### HasMessageId

`func (o *StreamMessageSendResponseResult) HasMessageId() bool`

HasMessageId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



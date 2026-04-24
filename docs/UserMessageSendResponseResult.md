# UserMessageSendResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageIds** | Pointer to [**[]MessageUserDelivery**](MessageUserDelivery.md) |  | [optional] 

## Methods

### NewUserMessageSendResponseResult

`func NewUserMessageSendResponseResult() *UserMessageSendResponseResult`

NewUserMessageSendResponseResult instantiates a new UserMessageSendResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserMessageSendResponseResultWithDefaults

`func NewUserMessageSendResponseResultWithDefaults() *UserMessageSendResponseResult`

NewUserMessageSendResponseResultWithDefaults instantiates a new UserMessageSendResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageIds

`func (o *UserMessageSendResponseResult) GetMessageIds() []MessageUserDelivery`

GetMessageIds returns the MessageIds field if non-nil, zero value otherwise.

### GetMessageIdsOk

`func (o *UserMessageSendResponseResult) GetMessageIdsOk() (*[]MessageUserDelivery, bool)`

GetMessageIdsOk returns a tuple with the MessageIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageIds

`func (o *UserMessageSendResponseResult) SetMessageIds(v []MessageUserDelivery)`

SetMessageIds sets MessageIds field to given value.

### HasMessageIds

`func (o *UserMessageSendResponseResult) HasMessageIds() bool`

HasMessageIds returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



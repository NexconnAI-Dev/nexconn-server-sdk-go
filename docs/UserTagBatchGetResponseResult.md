# UserTagBatchGetResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Users** | Pointer to [**[]UserTagBatchGetItem**](UserTagBatchGetItem.md) |  | [optional] 

## Methods

### NewUserTagBatchGetResponseResult

`func NewUserTagBatchGetResponseResult() *UserTagBatchGetResponseResult`

NewUserTagBatchGetResponseResult instantiates a new UserTagBatchGetResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserTagBatchGetResponseResultWithDefaults

`func NewUserTagBatchGetResponseResultWithDefaults() *UserTagBatchGetResponseResult`

NewUserTagBatchGetResponseResultWithDefaults instantiates a new UserTagBatchGetResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUsers

`func (o *UserTagBatchGetResponseResult) GetUsers() []UserTagBatchGetItem`

GetUsers returns the Users field if non-nil, zero value otherwise.

### GetUsersOk

`func (o *UserTagBatchGetResponseResult) GetUsersOk() (*[]UserTagBatchGetItem, bool)`

GetUsersOk returns a tuple with the Users field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUsers

`func (o *UserTagBatchGetResponseResult) SetUsers(v []UserTagBatchGetItem)`

SetUsers sets Users field to given value.

### HasUsers

`func (o *UserTagBatchGetResponseResult) HasUsers() bool`

HasUsers returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



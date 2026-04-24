# UserTagBatchGetItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**Tags** | Pointer to **[]string** |  | [optional] 

## Methods

### NewUserTagBatchGetItem

`func NewUserTagBatchGetItem() *UserTagBatchGetItem`

NewUserTagBatchGetItem instantiates a new UserTagBatchGetItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserTagBatchGetItemWithDefaults

`func NewUserTagBatchGetItemWithDefaults() *UserTagBatchGetItem`

NewUserTagBatchGetItemWithDefaults instantiates a new UserTagBatchGetItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserTagBatchGetItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserTagBatchGetItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserTagBatchGetItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *UserTagBatchGetItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetTags

`func (o *UserTagBatchGetItem) GetTags() []string`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *UserTagBatchGetItem) GetTagsOk() (*[]string, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *UserTagBatchGetItem) SetTags(v []string)`

SetTags sets Tags field to given value.

### HasTags

`func (o *UserTagBatchGetItem) HasTags() bool`

HasTags returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



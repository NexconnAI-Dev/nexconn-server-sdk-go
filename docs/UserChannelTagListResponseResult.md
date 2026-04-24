# UserChannelTagListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**Tags** | Pointer to [**[]UserChannelTagListItem**](UserChannelTagListItem.md) |  | [optional] 

## Methods

### NewUserChannelTagListResponseResult

`func NewUserChannelTagListResponseResult() *UserChannelTagListResponseResult`

NewUserChannelTagListResponseResult instantiates a new UserChannelTagListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserChannelTagListResponseResultWithDefaults

`func NewUserChannelTagListResponseResultWithDefaults() *UserChannelTagListResponseResult`

NewUserChannelTagListResponseResultWithDefaults instantiates a new UserChannelTagListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserChannelTagListResponseResult) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserChannelTagListResponseResult) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserChannelTagListResponseResult) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *UserChannelTagListResponseResult) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetTags

`func (o *UserChannelTagListResponseResult) GetTags() []UserChannelTagListItem`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *UserChannelTagListResponseResult) GetTagsOk() (*[]UserChannelTagListItem, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *UserChannelTagListResponseResult) SetTags(v []UserChannelTagListItem)`

SetTags sets Tags field to given value.

### HasTags

`func (o *UserChannelTagListResponseResult) HasTags() bool`

HasTags returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



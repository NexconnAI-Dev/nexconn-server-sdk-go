# UserChannelTagAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**Tags** | [**[]UserChannelTagItem**](UserChannelTagItem.md) |  | 

## Methods

### NewUserChannelTagAddRequest

`func NewUserChannelTagAddRequest(userId string, tags []UserChannelTagItem, ) *UserChannelTagAddRequest`

NewUserChannelTagAddRequest instantiates a new UserChannelTagAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserChannelTagAddRequestWithDefaults

`func NewUserChannelTagAddRequestWithDefaults() *UserChannelTagAddRequest`

NewUserChannelTagAddRequestWithDefaults instantiates a new UserChannelTagAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserChannelTagAddRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserChannelTagAddRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserChannelTagAddRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTags

`func (o *UserChannelTagAddRequest) GetTags() []UserChannelTagItem`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *UserChannelTagAddRequest) GetTagsOk() (*[]UserChannelTagItem, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *UserChannelTagAddRequest) SetTags(v []UserChannelTagItem)`

SetTags sets Tags field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



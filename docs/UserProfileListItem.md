# UserProfileListItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**Version** | Pointer to **int64** | Profile version from &#x60;UserProfileItemResult&#x60;. | [optional] 
**UserProfile** | Pointer to **map[string]interface{}** |  | [optional] 
**UserExtProfile** | Pointer to **map[string]interface{}** |  | [optional] 

## Methods

### NewUserProfileListItem

`func NewUserProfileListItem() *UserProfileListItem`

NewUserProfileListItem instantiates a new UserProfileListItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserProfileListItemWithDefaults

`func NewUserProfileListItemWithDefaults() *UserProfileListItem`

NewUserProfileListItemWithDefaults instantiates a new UserProfileListItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserProfileListItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserProfileListItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserProfileListItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *UserProfileListItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetVersion

`func (o *UserProfileListItem) GetVersion() int64`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *UserProfileListItem) GetVersionOk() (*int64, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *UserProfileListItem) SetVersion(v int64)`

SetVersion sets Version field to given value.

### HasVersion

`func (o *UserProfileListItem) HasVersion() bool`

HasVersion returns a boolean if a field has been set.

### GetUserProfile

`func (o *UserProfileListItem) GetUserProfile() map[string]interface{}`

GetUserProfile returns the UserProfile field if non-nil, zero value otherwise.

### GetUserProfileOk

`func (o *UserProfileListItem) GetUserProfileOk() (*map[string]interface{}, bool)`

GetUserProfileOk returns a tuple with the UserProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserProfile

`func (o *UserProfileListItem) SetUserProfile(v map[string]interface{})`

SetUserProfile sets UserProfile field to given value.

### HasUserProfile

`func (o *UserProfileListItem) HasUserProfile() bool`

HasUserProfile returns a boolean if a field has been set.

### GetUserExtProfile

`func (o *UserProfileListItem) GetUserExtProfile() map[string]interface{}`

GetUserExtProfile returns the UserExtProfile field if non-nil, zero value otherwise.

### GetUserExtProfileOk

`func (o *UserProfileListItem) GetUserExtProfileOk() (*map[string]interface{}, bool)`

GetUserExtProfileOk returns a tuple with the UserExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserExtProfile

`func (o *UserProfileListItem) SetUserExtProfile(v map[string]interface{})`

SetUserExtProfile sets UserExtProfile field to given value.

### HasUserExtProfile

`func (o *UserProfileListItem) HasUserExtProfile() bool`

HasUserExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



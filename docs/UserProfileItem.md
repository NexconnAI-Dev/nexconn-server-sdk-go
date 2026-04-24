# UserProfileItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**Version** | Pointer to **int64** |  | [optional] 
**UserProfile** | Pointer to **map[string]interface{}** |  | [optional] 
**UserExtProfile** | Pointer to **map[string]interface{}** |  | [optional] 

## Methods

### NewUserProfileItem

`func NewUserProfileItem() *UserProfileItem`

NewUserProfileItem instantiates a new UserProfileItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserProfileItemWithDefaults

`func NewUserProfileItemWithDefaults() *UserProfileItem`

NewUserProfileItemWithDefaults instantiates a new UserProfileItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserProfileItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserProfileItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserProfileItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *UserProfileItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetVersion

`func (o *UserProfileItem) GetVersion() int64`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *UserProfileItem) GetVersionOk() (*int64, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *UserProfileItem) SetVersion(v int64)`

SetVersion sets Version field to given value.

### HasVersion

`func (o *UserProfileItem) HasVersion() bool`

HasVersion returns a boolean if a field has been set.

### GetUserProfile

`func (o *UserProfileItem) GetUserProfile() map[string]interface{}`

GetUserProfile returns the UserProfile field if non-nil, zero value otherwise.

### GetUserProfileOk

`func (o *UserProfileItem) GetUserProfileOk() (*map[string]interface{}, bool)`

GetUserProfileOk returns a tuple with the UserProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserProfile

`func (o *UserProfileItem) SetUserProfile(v map[string]interface{})`

SetUserProfile sets UserProfile field to given value.

### HasUserProfile

`func (o *UserProfileItem) HasUserProfile() bool`

HasUserProfile returns a boolean if a field has been set.

### GetUserExtProfile

`func (o *UserProfileItem) GetUserExtProfile() map[string]interface{}`

GetUserExtProfile returns the UserExtProfile field if non-nil, zero value otherwise.

### GetUserExtProfileOk

`func (o *UserProfileItem) GetUserExtProfileOk() (*map[string]interface{}, bool)`

GetUserExtProfileOk returns a tuple with the UserExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserExtProfile

`func (o *UserProfileItem) SetUserExtProfile(v map[string]interface{})`

SetUserExtProfile sets UserExtProfile field to given value.

### HasUserExtProfile

`func (o *UserProfileItem) HasUserExtProfile() bool`

HasUserExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



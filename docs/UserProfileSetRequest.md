# UserProfileSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**UserProfile** | Pointer to **map[string]interface{}** | Basic profile payload. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided. | [optional] 
**UserExtProfile** | Pointer to **map[string]string** | Extended profile payload. Keys are case-sensitive, should use the &#x60;ext_&#x60; prefix, and values must be strings. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided.  | [optional] 

## Methods

### NewUserProfileSetRequest

`func NewUserProfileSetRequest(userId string, ) *UserProfileSetRequest`

NewUserProfileSetRequest instantiates a new UserProfileSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserProfileSetRequestWithDefaults

`func NewUserProfileSetRequestWithDefaults() *UserProfileSetRequest`

NewUserProfileSetRequestWithDefaults instantiates a new UserProfileSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserProfileSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserProfileSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserProfileSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetUserProfile

`func (o *UserProfileSetRequest) GetUserProfile() map[string]interface{}`

GetUserProfile returns the UserProfile field if non-nil, zero value otherwise.

### GetUserProfileOk

`func (o *UserProfileSetRequest) GetUserProfileOk() (*map[string]interface{}, bool)`

GetUserProfileOk returns a tuple with the UserProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserProfile

`func (o *UserProfileSetRequest) SetUserProfile(v map[string]interface{})`

SetUserProfile sets UserProfile field to given value.

### HasUserProfile

`func (o *UserProfileSetRequest) HasUserProfile() bool`

HasUserProfile returns a boolean if a field has been set.

### GetUserExtProfile

`func (o *UserProfileSetRequest) GetUserExtProfile() map[string]string`

GetUserExtProfile returns the UserExtProfile field if non-nil, zero value otherwise.

### GetUserExtProfileOk

`func (o *UserProfileSetRequest) GetUserExtProfileOk() (*map[string]string, bool)`

GetUserExtProfileOk returns a tuple with the UserExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserExtProfile

`func (o *UserProfileSetRequest) SetUserExtProfile(v map[string]string)`

SetUserExtProfile sets UserExtProfile field to given value.

### HasUserExtProfile

`func (o *UserProfileSetRequest) HasUserExtProfile() bool`

HasUserExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



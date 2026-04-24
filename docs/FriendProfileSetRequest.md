# FriendProfileSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TargetId** | **string** |  | 
**Alias** | Pointer to **string** | Omit this field to clear the existing alias. | [optional] 
**FriendExtProfile** | Pointer to **map[string]string** | Custom friend extension attributes. Keys should match &#x60;ext_xxxxx&#x60;, may contain letters, digits, and underscores, and support up to 10 entries.  | [optional] 

## Methods

### NewFriendProfileSetRequest

`func NewFriendProfileSetRequest(userId string, targetId string, ) *FriendProfileSetRequest`

NewFriendProfileSetRequest instantiates a new FriendProfileSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendProfileSetRequestWithDefaults

`func NewFriendProfileSetRequestWithDefaults() *FriendProfileSetRequest`

NewFriendProfileSetRequestWithDefaults instantiates a new FriendProfileSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendProfileSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendProfileSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendProfileSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTargetId

`func (o *FriendProfileSetRequest) GetTargetId() string`

GetTargetId returns the TargetId field if non-nil, zero value otherwise.

### GetTargetIdOk

`func (o *FriendProfileSetRequest) GetTargetIdOk() (*string, bool)`

GetTargetIdOk returns a tuple with the TargetId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetId

`func (o *FriendProfileSetRequest) SetTargetId(v string)`

SetTargetId sets TargetId field to given value.


### GetAlias

`func (o *FriendProfileSetRequest) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *FriendProfileSetRequest) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *FriendProfileSetRequest) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *FriendProfileSetRequest) HasAlias() bool`

HasAlias returns a boolean if a field has been set.

### GetFriendExtProfile

`func (o *FriendProfileSetRequest) GetFriendExtProfile() map[string]string`

GetFriendExtProfile returns the FriendExtProfile field if non-nil, zero value otherwise.

### GetFriendExtProfileOk

`func (o *FriendProfileSetRequest) GetFriendExtProfileOk() (*map[string]string, bool)`

GetFriendExtProfileOk returns a tuple with the FriendExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFriendExtProfile

`func (o *FriendProfileSetRequest) SetFriendExtProfile(v map[string]string)`

SetFriendExtProfile sets FriendExtProfile field to given value.

### HasFriendExtProfile

`func (o *FriendProfileSetRequest) HasFriendExtProfile() bool`

HasFriendExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



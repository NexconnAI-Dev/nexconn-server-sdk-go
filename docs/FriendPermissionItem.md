# FriendPermissionItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**PermissionType** | Pointer to **int32** |  | [optional] 

## Methods

### NewFriendPermissionItem

`func NewFriendPermissionItem() *FriendPermissionItem`

NewFriendPermissionItem instantiates a new FriendPermissionItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendPermissionItemWithDefaults

`func NewFriendPermissionItemWithDefaults() *FriendPermissionItem`

NewFriendPermissionItemWithDefaults instantiates a new FriendPermissionItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendPermissionItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendPermissionItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendPermissionItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *FriendPermissionItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetPermissionType

`func (o *FriendPermissionItem) GetPermissionType() int32`

GetPermissionType returns the PermissionType field if non-nil, zero value otherwise.

### GetPermissionTypeOk

`func (o *FriendPermissionItem) GetPermissionTypeOk() (*int32, bool)`

GetPermissionTypeOk returns a tuple with the PermissionType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissionType

`func (o *FriendPermissionItem) SetPermissionType(v int32)`

SetPermissionType sets PermissionType field to given value.

### HasPermissionType

`func (o *FriendPermissionItem) HasPermissionType() bool`

HasPermissionType returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



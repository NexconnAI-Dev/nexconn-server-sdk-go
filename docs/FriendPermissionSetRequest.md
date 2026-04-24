# FriendPermissionSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserIds** | **[]string** |  | 
**PermissionType** | **int32** | &#x60;1&#x60; allows everyone, &#x60;2&#x60; requires approval, and &#x60;3&#x60; rejects all requests. | 

## Methods

### NewFriendPermissionSetRequest

`func NewFriendPermissionSetRequest(userIds []string, permissionType int32, ) *FriendPermissionSetRequest`

NewFriendPermissionSetRequest instantiates a new FriendPermissionSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendPermissionSetRequestWithDefaults

`func NewFriendPermissionSetRequestWithDefaults() *FriendPermissionSetRequest`

NewFriendPermissionSetRequestWithDefaults instantiates a new FriendPermissionSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserIds

`func (o *FriendPermissionSetRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *FriendPermissionSetRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *FriendPermissionSetRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetPermissionType

`func (o *FriendPermissionSetRequest) GetPermissionType() int32`

GetPermissionType returns the PermissionType field if non-nil, zero value otherwise.

### GetPermissionTypeOk

`func (o *FriendPermissionSetRequest) GetPermissionTypeOk() (*int32, bool)`

GetPermissionTypeOk returns a tuple with the PermissionType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissionType

`func (o *FriendPermissionSetRequest) SetPermissionType(v int32)`

SetPermissionType sets PermissionType field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



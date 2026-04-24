# GroupChannelProfileItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Group channel ID. | [optional] 
**Name** | Pointer to **string** | Group name. | [optional] 
**GroupProfile** | Pointer to **map[string]interface{}** | Group basic profile JSON object, such as introduction, announcement, and portrait URL. | [optional] 
**GroupExtProfile** | Pointer to **map[string]interface{}** | Extended group profile JSON object. Keys are typically custom fields prefixed with &#x60;ext_&#x60;. | [optional] 
**Permissions** | Pointer to **map[string]interface{}** | Group permission settings JSON object, including join, invite, and profile-management permissions. | [optional] 
**Owner** | Pointer to **string** | User ID of the current group owner. | [optional] 
**CreatedAt** | Pointer to **int64** | Timestamp when the group was created. | [optional] 
**MemberCount** | Pointer to **int32** | Current number of group members. | [optional] 

## Methods

### NewGroupChannelProfileItem

`func NewGroupChannelProfileItem() *GroupChannelProfileItem`

NewGroupChannelProfileItem instantiates a new GroupChannelProfileItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelProfileItemWithDefaults

`func NewGroupChannelProfileItemWithDefaults() *GroupChannelProfileItem`

NewGroupChannelProfileItemWithDefaults instantiates a new GroupChannelProfileItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelProfileItem) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelProfileItem) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelProfileItem) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelProfileItem) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetName

`func (o *GroupChannelProfileItem) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *GroupChannelProfileItem) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *GroupChannelProfileItem) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *GroupChannelProfileItem) HasName() bool`

HasName returns a boolean if a field has been set.

### GetGroupProfile

`func (o *GroupChannelProfileItem) GetGroupProfile() map[string]interface{}`

GetGroupProfile returns the GroupProfile field if non-nil, zero value otherwise.

### GetGroupProfileOk

`func (o *GroupChannelProfileItem) GetGroupProfileOk() (*map[string]interface{}, bool)`

GetGroupProfileOk returns a tuple with the GroupProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupProfile

`func (o *GroupChannelProfileItem) SetGroupProfile(v map[string]interface{})`

SetGroupProfile sets GroupProfile field to given value.

### HasGroupProfile

`func (o *GroupChannelProfileItem) HasGroupProfile() bool`

HasGroupProfile returns a boolean if a field has been set.

### GetGroupExtProfile

`func (o *GroupChannelProfileItem) GetGroupExtProfile() map[string]interface{}`

GetGroupExtProfile returns the GroupExtProfile field if non-nil, zero value otherwise.

### GetGroupExtProfileOk

`func (o *GroupChannelProfileItem) GetGroupExtProfileOk() (*map[string]interface{}, bool)`

GetGroupExtProfileOk returns a tuple with the GroupExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupExtProfile

`func (o *GroupChannelProfileItem) SetGroupExtProfile(v map[string]interface{})`

SetGroupExtProfile sets GroupExtProfile field to given value.

### HasGroupExtProfile

`func (o *GroupChannelProfileItem) HasGroupExtProfile() bool`

HasGroupExtProfile returns a boolean if a field has been set.

### GetPermissions

`func (o *GroupChannelProfileItem) GetPermissions() map[string]interface{}`

GetPermissions returns the Permissions field if non-nil, zero value otherwise.

### GetPermissionsOk

`func (o *GroupChannelProfileItem) GetPermissionsOk() (*map[string]interface{}, bool)`

GetPermissionsOk returns a tuple with the Permissions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissions

`func (o *GroupChannelProfileItem) SetPermissions(v map[string]interface{})`

SetPermissions sets Permissions field to given value.

### HasPermissions

`func (o *GroupChannelProfileItem) HasPermissions() bool`

HasPermissions returns a boolean if a field has been set.

### GetOwner

`func (o *GroupChannelProfileItem) GetOwner() string`

GetOwner returns the Owner field if non-nil, zero value otherwise.

### GetOwnerOk

`func (o *GroupChannelProfileItem) GetOwnerOk() (*string, bool)`

GetOwnerOk returns a tuple with the Owner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOwner

`func (o *GroupChannelProfileItem) SetOwner(v string)`

SetOwner sets Owner field to given value.

### HasOwner

`func (o *GroupChannelProfileItem) HasOwner() bool`

HasOwner returns a boolean if a field has been set.

### GetCreatedAt

`func (o *GroupChannelProfileItem) GetCreatedAt() int64`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *GroupChannelProfileItem) GetCreatedAtOk() (*int64, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *GroupChannelProfileItem) SetCreatedAt(v int64)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *GroupChannelProfileItem) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.

### GetMemberCount

`func (o *GroupChannelProfileItem) GetMemberCount() int32`

GetMemberCount returns the MemberCount field if non-nil, zero value otherwise.

### GetMemberCountOk

`func (o *GroupChannelProfileItem) GetMemberCountOk() (*int32, bool)`

GetMemberCountOk returns a tuple with the MemberCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMemberCount

`func (o *GroupChannelProfileItem) SetMemberCount(v int32)`

SetMemberCount sets MemberCount field to given value.

### HasMemberCount

`func (o *GroupChannelProfileItem) HasMemberCount() bool`

HasMemberCount returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# GroupChannelJoinedItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Group channel ID. | [optional] 
**Name** | Pointer to **string** | Group name. | [optional] 
**GroupProfile** | Pointer to **map[string]interface{}** | Group basic profile JSON object. | [optional] 
**GroupExtProfile** | Pointer to **map[string]interface{}** | Group extended profile JSON object. | [optional] 
**Permissions** | Pointer to **map[string]interface{}** | Group permission settings JSON object. | [optional] 
**Alias** | Pointer to **string** | Group alias or remark name set by the querying user. | [optional] 
**Owner** | Pointer to **string** | User ID of the current group owner. | [optional] 
**MemberCount** | Pointer to **int32** | Number of members in the group. | [optional] 
**JoinedAt** | Pointer to **int64** | Timestamp when the querying user joined the group. | [optional] 
**Role** | Pointer to **int32** | The querying user&#39;s role in the group. &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] 
**CreatedAt** | Pointer to **int64** | Timestamp when the group was created. | [optional] 

## Methods

### NewGroupChannelJoinedItem

`func NewGroupChannelJoinedItem() *GroupChannelJoinedItem`

NewGroupChannelJoinedItem instantiates a new GroupChannelJoinedItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelJoinedItemWithDefaults

`func NewGroupChannelJoinedItemWithDefaults() *GroupChannelJoinedItem`

NewGroupChannelJoinedItemWithDefaults instantiates a new GroupChannelJoinedItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelJoinedItem) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelJoinedItem) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelJoinedItem) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelJoinedItem) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetName

`func (o *GroupChannelJoinedItem) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *GroupChannelJoinedItem) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *GroupChannelJoinedItem) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *GroupChannelJoinedItem) HasName() bool`

HasName returns a boolean if a field has been set.

### GetGroupProfile

`func (o *GroupChannelJoinedItem) GetGroupProfile() map[string]interface{}`

GetGroupProfile returns the GroupProfile field if non-nil, zero value otherwise.

### GetGroupProfileOk

`func (o *GroupChannelJoinedItem) GetGroupProfileOk() (*map[string]interface{}, bool)`

GetGroupProfileOk returns a tuple with the GroupProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupProfile

`func (o *GroupChannelJoinedItem) SetGroupProfile(v map[string]interface{})`

SetGroupProfile sets GroupProfile field to given value.

### HasGroupProfile

`func (o *GroupChannelJoinedItem) HasGroupProfile() bool`

HasGroupProfile returns a boolean if a field has been set.

### GetGroupExtProfile

`func (o *GroupChannelJoinedItem) GetGroupExtProfile() map[string]interface{}`

GetGroupExtProfile returns the GroupExtProfile field if non-nil, zero value otherwise.

### GetGroupExtProfileOk

`func (o *GroupChannelJoinedItem) GetGroupExtProfileOk() (*map[string]interface{}, bool)`

GetGroupExtProfileOk returns a tuple with the GroupExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupExtProfile

`func (o *GroupChannelJoinedItem) SetGroupExtProfile(v map[string]interface{})`

SetGroupExtProfile sets GroupExtProfile field to given value.

### HasGroupExtProfile

`func (o *GroupChannelJoinedItem) HasGroupExtProfile() bool`

HasGroupExtProfile returns a boolean if a field has been set.

### GetPermissions

`func (o *GroupChannelJoinedItem) GetPermissions() map[string]interface{}`

GetPermissions returns the Permissions field if non-nil, zero value otherwise.

### GetPermissionsOk

`func (o *GroupChannelJoinedItem) GetPermissionsOk() (*map[string]interface{}, bool)`

GetPermissionsOk returns a tuple with the Permissions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissions

`func (o *GroupChannelJoinedItem) SetPermissions(v map[string]interface{})`

SetPermissions sets Permissions field to given value.

### HasPermissions

`func (o *GroupChannelJoinedItem) HasPermissions() bool`

HasPermissions returns a boolean if a field has been set.

### GetAlias

`func (o *GroupChannelJoinedItem) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *GroupChannelJoinedItem) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *GroupChannelJoinedItem) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *GroupChannelJoinedItem) HasAlias() bool`

HasAlias returns a boolean if a field has been set.

### GetOwner

`func (o *GroupChannelJoinedItem) GetOwner() string`

GetOwner returns the Owner field if non-nil, zero value otherwise.

### GetOwnerOk

`func (o *GroupChannelJoinedItem) GetOwnerOk() (*string, bool)`

GetOwnerOk returns a tuple with the Owner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOwner

`func (o *GroupChannelJoinedItem) SetOwner(v string)`

SetOwner sets Owner field to given value.

### HasOwner

`func (o *GroupChannelJoinedItem) HasOwner() bool`

HasOwner returns a boolean if a field has been set.

### GetMemberCount

`func (o *GroupChannelJoinedItem) GetMemberCount() int32`

GetMemberCount returns the MemberCount field if non-nil, zero value otherwise.

### GetMemberCountOk

`func (o *GroupChannelJoinedItem) GetMemberCountOk() (*int32, bool)`

GetMemberCountOk returns a tuple with the MemberCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMemberCount

`func (o *GroupChannelJoinedItem) SetMemberCount(v int32)`

SetMemberCount sets MemberCount field to given value.

### HasMemberCount

`func (o *GroupChannelJoinedItem) HasMemberCount() bool`

HasMemberCount returns a boolean if a field has been set.

### GetJoinedAt

`func (o *GroupChannelJoinedItem) GetJoinedAt() int64`

GetJoinedAt returns the JoinedAt field if non-nil, zero value otherwise.

### GetJoinedAtOk

`func (o *GroupChannelJoinedItem) GetJoinedAtOk() (*int64, bool)`

GetJoinedAtOk returns a tuple with the JoinedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJoinedAt

`func (o *GroupChannelJoinedItem) SetJoinedAt(v int64)`

SetJoinedAt sets JoinedAt field to given value.

### HasJoinedAt

`func (o *GroupChannelJoinedItem) HasJoinedAt() bool`

HasJoinedAt returns a boolean if a field has been set.

### GetRole

`func (o *GroupChannelJoinedItem) GetRole() int32`

GetRole returns the Role field if non-nil, zero value otherwise.

### GetRoleOk

`func (o *GroupChannelJoinedItem) GetRoleOk() (*int32, bool)`

GetRoleOk returns a tuple with the Role field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRole

`func (o *GroupChannelJoinedItem) SetRole(v int32)`

SetRole sets Role field to given value.

### HasRole

`func (o *GroupChannelJoinedItem) HasRole() bool`

HasRole returns a boolean if a field has been set.

### GetCreatedAt

`func (o *GroupChannelJoinedItem) GetCreatedAt() int64`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *GroupChannelJoinedItem) GetCreatedAtOk() (*int64, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *GroupChannelJoinedItem) SetCreatedAt(v int64)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *GroupChannelJoinedItem) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



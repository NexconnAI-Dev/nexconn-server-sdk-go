# GroupChannelMemberItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** | Member user ID. | [optional] 
**Role** | Pointer to **int32** | Member role. &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] 
**Nickname** | Pointer to **string** | Member nickname in the group. | [optional] 
**Extra** | Pointer to **string** | Additional member profile information. | [optional] 
**JoinedAt** | Pointer to **int64** | Timestamp when the member joined the group. | [optional] 

## Methods

### NewGroupChannelMemberItem

`func NewGroupChannelMemberItem() *GroupChannelMemberItem`

NewGroupChannelMemberItem instantiates a new GroupChannelMemberItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberItemWithDefaults

`func NewGroupChannelMemberItemWithDefaults() *GroupChannelMemberItem`

NewGroupChannelMemberItemWithDefaults instantiates a new GroupChannelMemberItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *GroupChannelMemberItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelMemberItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelMemberItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *GroupChannelMemberItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetRole

`func (o *GroupChannelMemberItem) GetRole() int32`

GetRole returns the Role field if non-nil, zero value otherwise.

### GetRoleOk

`func (o *GroupChannelMemberItem) GetRoleOk() (*int32, bool)`

GetRoleOk returns a tuple with the Role field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRole

`func (o *GroupChannelMemberItem) SetRole(v int32)`

SetRole sets Role field to given value.

### HasRole

`func (o *GroupChannelMemberItem) HasRole() bool`

HasRole returns a boolean if a field has been set.

### GetNickname

`func (o *GroupChannelMemberItem) GetNickname() string`

GetNickname returns the Nickname field if non-nil, zero value otherwise.

### GetNicknameOk

`func (o *GroupChannelMemberItem) GetNicknameOk() (*string, bool)`

GetNicknameOk returns a tuple with the Nickname field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNickname

`func (o *GroupChannelMemberItem) SetNickname(v string)`

SetNickname sets Nickname field to given value.

### HasNickname

`func (o *GroupChannelMemberItem) HasNickname() bool`

HasNickname returns a boolean if a field has been set.

### GetExtra

`func (o *GroupChannelMemberItem) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *GroupChannelMemberItem) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *GroupChannelMemberItem) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *GroupChannelMemberItem) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetJoinedAt

`func (o *GroupChannelMemberItem) GetJoinedAt() int64`

GetJoinedAt returns the JoinedAt field if non-nil, zero value otherwise.

### GetJoinedAtOk

`func (o *GroupChannelMemberItem) GetJoinedAtOk() (*int64, bool)`

GetJoinedAtOk returns a tuple with the JoinedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJoinedAt

`func (o *GroupChannelMemberItem) SetJoinedAt(v int64)`

SetJoinedAt sets JoinedAt field to given value.

### HasJoinedAt

`func (o *GroupChannelMemberItem) HasJoinedAt() bool`

HasJoinedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



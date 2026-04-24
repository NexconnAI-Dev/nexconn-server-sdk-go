# GroupChannelMutedMemberItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**MutedAt** | Pointer to **string** | Mute start time in &#x60;YYYY-MM-DD HH:MM:SS&#x60; format. | [optional] 
**MuteExpiresAt** | Pointer to **string** | Mute expiry time in &#x60;YYYY-MM-DD HH:MM:SS&#x60; format. | [optional] 

## Methods

### NewGroupChannelMutedMemberItem

`func NewGroupChannelMutedMemberItem() *GroupChannelMutedMemberItem`

NewGroupChannelMutedMemberItem instantiates a new GroupChannelMutedMemberItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMutedMemberItemWithDefaults

`func NewGroupChannelMutedMemberItemWithDefaults() *GroupChannelMutedMemberItem`

NewGroupChannelMutedMemberItemWithDefaults instantiates a new GroupChannelMutedMemberItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *GroupChannelMutedMemberItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelMutedMemberItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelMutedMemberItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *GroupChannelMutedMemberItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetMutedAt

`func (o *GroupChannelMutedMemberItem) GetMutedAt() string`

GetMutedAt returns the MutedAt field if non-nil, zero value otherwise.

### GetMutedAtOk

`func (o *GroupChannelMutedMemberItem) GetMutedAtOk() (*string, bool)`

GetMutedAtOk returns a tuple with the MutedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMutedAt

`func (o *GroupChannelMutedMemberItem) SetMutedAt(v string)`

SetMutedAt sets MutedAt field to given value.

### HasMutedAt

`func (o *GroupChannelMutedMemberItem) HasMutedAt() bool`

HasMutedAt returns a boolean if a field has been set.

### GetMuteExpiresAt

`func (o *GroupChannelMutedMemberItem) GetMuteExpiresAt() string`

GetMuteExpiresAt returns the MuteExpiresAt field if non-nil, zero value otherwise.

### GetMuteExpiresAtOk

`func (o *GroupChannelMutedMemberItem) GetMuteExpiresAtOk() (*string, bool)`

GetMuteExpiresAtOk returns a tuple with the MuteExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMuteExpiresAt

`func (o *GroupChannelMutedMemberItem) SetMuteExpiresAt(v string)`

SetMuteExpiresAt sets MuteExpiresAt field to given value.

### HasMuteExpiresAt

`func (o *GroupChannelMutedMemberItem) HasMuteExpiresAt() bool`

HasMuteExpiresAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



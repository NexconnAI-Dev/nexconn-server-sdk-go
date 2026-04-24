# GroupChannelMemberSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserId** | **string** |  | 
**Nickname** | Pointer to **string** |  | [optional] 
**Extra** | Pointer to **string** | Member extra profile string defined by the source API. | [optional] 

## Methods

### NewGroupChannelMemberSetRequest

`func NewGroupChannelMemberSetRequest(channelId string, userId string, ) *GroupChannelMemberSetRequest`

NewGroupChannelMemberSetRequest instantiates a new GroupChannelMemberSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberSetRequestWithDefaults

`func NewGroupChannelMemberSetRequestWithDefaults() *GroupChannelMemberSetRequest`

NewGroupChannelMemberSetRequestWithDefaults instantiates a new GroupChannelMemberSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelMemberSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelMemberSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelMemberSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserId

`func (o *GroupChannelMemberSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelMemberSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelMemberSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetNickname

`func (o *GroupChannelMemberSetRequest) GetNickname() string`

GetNickname returns the Nickname field if non-nil, zero value otherwise.

### GetNicknameOk

`func (o *GroupChannelMemberSetRequest) GetNicknameOk() (*string, bool)`

GetNicknameOk returns a tuple with the Nickname field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNickname

`func (o *GroupChannelMemberSetRequest) SetNickname(v string)`

SetNickname sets Nickname field to given value.

### HasNickname

`func (o *GroupChannelMemberSetRequest) HasNickname() bool`

HasNickname returns a boolean if a field has been set.

### GetExtra

`func (o *GroupChannelMemberSetRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *GroupChannelMemberSetRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *GroupChannelMemberSetRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *GroupChannelMemberSetRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



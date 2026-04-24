# GroupChannelQuitRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserIds** | **[]string** |  | 
**ShouldDeleteMute** | Pointer to **int32** | &#x60;0&#x60; means keep each leaving member&#39;s mute state and &#x60;1&#x60; means remove it. | [optional] 
**ShouldDeleteAllowedSendersList** | Pointer to **int32** | &#x60;0&#x60; means keep each leaving member&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. | [optional] 
**ShouldDeleteFavorites** | Pointer to **int32** | &#x60;0&#x60; means keep each leaving member&#39;s favorites record and &#x60;1&#x60; means remove it. | [optional] 

## Methods

### NewGroupChannelQuitRequest

`func NewGroupChannelQuitRequest(channelId string, userIds []string, ) *GroupChannelQuitRequest`

NewGroupChannelQuitRequest instantiates a new GroupChannelQuitRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelQuitRequestWithDefaults

`func NewGroupChannelQuitRequestWithDefaults() *GroupChannelQuitRequest`

NewGroupChannelQuitRequestWithDefaults instantiates a new GroupChannelQuitRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelQuitRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelQuitRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelQuitRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserIds

`func (o *GroupChannelQuitRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *GroupChannelQuitRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *GroupChannelQuitRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetShouldDeleteMute

`func (o *GroupChannelQuitRequest) GetShouldDeleteMute() int32`

GetShouldDeleteMute returns the ShouldDeleteMute field if non-nil, zero value otherwise.

### GetShouldDeleteMuteOk

`func (o *GroupChannelQuitRequest) GetShouldDeleteMuteOk() (*int32, bool)`

GetShouldDeleteMuteOk returns a tuple with the ShouldDeleteMute field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteMute

`func (o *GroupChannelQuitRequest) SetShouldDeleteMute(v int32)`

SetShouldDeleteMute sets ShouldDeleteMute field to given value.

### HasShouldDeleteMute

`func (o *GroupChannelQuitRequest) HasShouldDeleteMute() bool`

HasShouldDeleteMute returns a boolean if a field has been set.

### GetShouldDeleteAllowedSendersList

`func (o *GroupChannelQuitRequest) GetShouldDeleteAllowedSendersList() int32`

GetShouldDeleteAllowedSendersList returns the ShouldDeleteAllowedSendersList field if non-nil, zero value otherwise.

### GetShouldDeleteAllowedSendersListOk

`func (o *GroupChannelQuitRequest) GetShouldDeleteAllowedSendersListOk() (*int32, bool)`

GetShouldDeleteAllowedSendersListOk returns a tuple with the ShouldDeleteAllowedSendersList field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteAllowedSendersList

`func (o *GroupChannelQuitRequest) SetShouldDeleteAllowedSendersList(v int32)`

SetShouldDeleteAllowedSendersList sets ShouldDeleteAllowedSendersList field to given value.

### HasShouldDeleteAllowedSendersList

`func (o *GroupChannelQuitRequest) HasShouldDeleteAllowedSendersList() bool`

HasShouldDeleteAllowedSendersList returns a boolean if a field has been set.

### GetShouldDeleteFavorites

`func (o *GroupChannelQuitRequest) GetShouldDeleteFavorites() int32`

GetShouldDeleteFavorites returns the ShouldDeleteFavorites field if non-nil, zero value otherwise.

### GetShouldDeleteFavoritesOk

`func (o *GroupChannelQuitRequest) GetShouldDeleteFavoritesOk() (*int32, bool)`

GetShouldDeleteFavoritesOk returns a tuple with the ShouldDeleteFavorites field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteFavorites

`func (o *GroupChannelQuitRequest) SetShouldDeleteFavorites(v int32)`

SetShouldDeleteFavorites sets ShouldDeleteFavorites field to given value.

### HasShouldDeleteFavorites

`func (o *GroupChannelQuitRequest) HasShouldDeleteFavorites() bool`

HasShouldDeleteFavorites returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



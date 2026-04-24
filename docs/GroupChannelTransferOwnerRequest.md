# GroupChannelTransferOwnerRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**NewOwner** | **string** |  | 
**ShouldLeave** | Pointer to **int32** | &#x60;0&#x60; means keep the previous owner in the group and &#x60;1&#x60; means leave the group. | [optional] 
**ShouldDeleteMute** | Pointer to **int32** | &#x60;0&#x60; means keep the previous owner&#39;s mute state and &#x60;1&#x60; means remove it. | [optional] 
**ShouldDeleteAllowedSendersList** | Pointer to **int32** | &#x60;0&#x60; means keep the previous owner&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. | [optional] 
**ShouldDeleteFavorites** | Pointer to **int32** | &#x60;0&#x60; means keep favorites and &#x60;1&#x60; means remove them. | [optional] 

## Methods

### NewGroupChannelTransferOwnerRequest

`func NewGroupChannelTransferOwnerRequest(channelId string, newOwner string, ) *GroupChannelTransferOwnerRequest`

NewGroupChannelTransferOwnerRequest instantiates a new GroupChannelTransferOwnerRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelTransferOwnerRequestWithDefaults

`func NewGroupChannelTransferOwnerRequestWithDefaults() *GroupChannelTransferOwnerRequest`

NewGroupChannelTransferOwnerRequestWithDefaults instantiates a new GroupChannelTransferOwnerRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelTransferOwnerRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelTransferOwnerRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelTransferOwnerRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetNewOwner

`func (o *GroupChannelTransferOwnerRequest) GetNewOwner() string`

GetNewOwner returns the NewOwner field if non-nil, zero value otherwise.

### GetNewOwnerOk

`func (o *GroupChannelTransferOwnerRequest) GetNewOwnerOk() (*string, bool)`

GetNewOwnerOk returns a tuple with the NewOwner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNewOwner

`func (o *GroupChannelTransferOwnerRequest) SetNewOwner(v string)`

SetNewOwner sets NewOwner field to given value.


### GetShouldLeave

`func (o *GroupChannelTransferOwnerRequest) GetShouldLeave() int32`

GetShouldLeave returns the ShouldLeave field if non-nil, zero value otherwise.

### GetShouldLeaveOk

`func (o *GroupChannelTransferOwnerRequest) GetShouldLeaveOk() (*int32, bool)`

GetShouldLeaveOk returns a tuple with the ShouldLeave field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldLeave

`func (o *GroupChannelTransferOwnerRequest) SetShouldLeave(v int32)`

SetShouldLeave sets ShouldLeave field to given value.

### HasShouldLeave

`func (o *GroupChannelTransferOwnerRequest) HasShouldLeave() bool`

HasShouldLeave returns a boolean if a field has been set.

### GetShouldDeleteMute

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteMute() int32`

GetShouldDeleteMute returns the ShouldDeleteMute field if non-nil, zero value otherwise.

### GetShouldDeleteMuteOk

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteMuteOk() (*int32, bool)`

GetShouldDeleteMuteOk returns a tuple with the ShouldDeleteMute field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteMute

`func (o *GroupChannelTransferOwnerRequest) SetShouldDeleteMute(v int32)`

SetShouldDeleteMute sets ShouldDeleteMute field to given value.

### HasShouldDeleteMute

`func (o *GroupChannelTransferOwnerRequest) HasShouldDeleteMute() bool`

HasShouldDeleteMute returns a boolean if a field has been set.

### GetShouldDeleteAllowedSendersList

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteAllowedSendersList() int32`

GetShouldDeleteAllowedSendersList returns the ShouldDeleteAllowedSendersList field if non-nil, zero value otherwise.

### GetShouldDeleteAllowedSendersListOk

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteAllowedSendersListOk() (*int32, bool)`

GetShouldDeleteAllowedSendersListOk returns a tuple with the ShouldDeleteAllowedSendersList field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteAllowedSendersList

`func (o *GroupChannelTransferOwnerRequest) SetShouldDeleteAllowedSendersList(v int32)`

SetShouldDeleteAllowedSendersList sets ShouldDeleteAllowedSendersList field to given value.

### HasShouldDeleteAllowedSendersList

`func (o *GroupChannelTransferOwnerRequest) HasShouldDeleteAllowedSendersList() bool`

HasShouldDeleteAllowedSendersList returns a boolean if a field has been set.

### GetShouldDeleteFavorites

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteFavorites() int32`

GetShouldDeleteFavorites returns the ShouldDeleteFavorites field if non-nil, zero value otherwise.

### GetShouldDeleteFavoritesOk

`func (o *GroupChannelTransferOwnerRequest) GetShouldDeleteFavoritesOk() (*int32, bool)`

GetShouldDeleteFavoritesOk returns a tuple with the ShouldDeleteFavorites field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldDeleteFavorites

`func (o *GroupChannelTransferOwnerRequest) SetShouldDeleteFavorites(v int32)`

SetShouldDeleteFavorites sets ShouldDeleteFavorites field to given value.

### HasShouldDeleteFavorites

`func (o *GroupChannelTransferOwnerRequest) HasShouldDeleteFavorites() bool`

HasShouldDeleteFavorites returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



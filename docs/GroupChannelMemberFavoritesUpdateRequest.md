# GroupChannelMemberFavoritesUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserId** | **string** |  | 
**FavoriteIds** | **[]string** | Followed member user IDs. | 

## Methods

### NewGroupChannelMemberFavoritesUpdateRequest

`func NewGroupChannelMemberFavoritesUpdateRequest(channelId string, userId string, favoriteIds []string, ) *GroupChannelMemberFavoritesUpdateRequest`

NewGroupChannelMemberFavoritesUpdateRequest instantiates a new GroupChannelMemberFavoritesUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberFavoritesUpdateRequestWithDefaults

`func NewGroupChannelMemberFavoritesUpdateRequestWithDefaults() *GroupChannelMemberFavoritesUpdateRequest`

NewGroupChannelMemberFavoritesUpdateRequestWithDefaults instantiates a new GroupChannelMemberFavoritesUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelMemberFavoritesUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserId

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelMemberFavoritesUpdateRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetFavoriteIds

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetFavoriteIds() []string`

GetFavoriteIds returns the FavoriteIds field if non-nil, zero value otherwise.

### GetFavoriteIdsOk

`func (o *GroupChannelMemberFavoritesUpdateRequest) GetFavoriteIdsOk() (*[]string, bool)`

GetFavoriteIdsOk returns a tuple with the FavoriteIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFavoriteIds

`func (o *GroupChannelMemberFavoritesUpdateRequest) SetFavoriteIds(v []string)`

SetFavoriteIds sets FavoriteIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



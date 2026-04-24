# GroupChannelMemberFavoritesListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**ChannelId** | Pointer to **string** |  | [optional] 
**Favorites** | Pointer to [**[]GroupChannelFavoriteItem**](GroupChannelFavoriteItem.md) |  | [optional] 

## Methods

### NewGroupChannelMemberFavoritesListResponseResult

`func NewGroupChannelMemberFavoritesListResponseResult() *GroupChannelMemberFavoritesListResponseResult`

NewGroupChannelMemberFavoritesListResponseResult instantiates a new GroupChannelMemberFavoritesListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberFavoritesListResponseResultWithDefaults

`func NewGroupChannelMemberFavoritesListResponseResultWithDefaults() *GroupChannelMemberFavoritesListResponseResult`

NewGroupChannelMemberFavoritesListResponseResultWithDefaults instantiates a new GroupChannelMemberFavoritesListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *GroupChannelMemberFavoritesListResponseResult) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelMemberFavoritesListResponseResult) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelMemberFavoritesListResponseResult) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *GroupChannelMemberFavoritesListResponseResult) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetChannelId

`func (o *GroupChannelMemberFavoritesListResponseResult) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelMemberFavoritesListResponseResult) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelMemberFavoritesListResponseResult) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelMemberFavoritesListResponseResult) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetFavorites

`func (o *GroupChannelMemberFavoritesListResponseResult) GetFavorites() []GroupChannelFavoriteItem`

GetFavorites returns the Favorites field if non-nil, zero value otherwise.

### GetFavoritesOk

`func (o *GroupChannelMemberFavoritesListResponseResult) GetFavoritesOk() (*[]GroupChannelFavoriteItem, bool)`

GetFavoritesOk returns a tuple with the Favorites field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFavorites

`func (o *GroupChannelMemberFavoritesListResponseResult) SetFavorites(v []GroupChannelFavoriteItem)`

SetFavorites sets Favorites field to given value.

### HasFavorites

`func (o *GroupChannelMemberFavoritesListResponseResult) HasFavorites() bool`

HasFavorites returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



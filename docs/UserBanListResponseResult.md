# UserBanListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BannedUsers** | Pointer to [**[]BannedUser**](BannedUser.md) |  | [optional] 

## Methods

### NewUserBanListResponseResult

`func NewUserBanListResponseResult() *UserBanListResponseResult`

NewUserBanListResponseResult instantiates a new UserBanListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBanListResponseResultWithDefaults

`func NewUserBanListResponseResultWithDefaults() *UserBanListResponseResult`

NewUserBanListResponseResultWithDefaults instantiates a new UserBanListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetBannedUsers

`func (o *UserBanListResponseResult) GetBannedUsers() []BannedUser`

GetBannedUsers returns the BannedUsers field if non-nil, zero value otherwise.

### GetBannedUsersOk

`func (o *UserBanListResponseResult) GetBannedUsersOk() (*[]BannedUser, bool)`

GetBannedUsersOk returns a tuple with the BannedUsers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBannedUsers

`func (o *UserBanListResponseResult) SetBannedUsers(v []BannedUser)`

SetBannedUsers sets BannedUsers field to given value.

### HasBannedUsers

`func (o *UserBanListResponseResult) HasBannedUsers() bool`

HasBannedUsers returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



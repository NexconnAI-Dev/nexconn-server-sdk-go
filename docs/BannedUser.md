# BannedUser

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**BanExpiresAt** | Pointer to **string** | Ban expiry time as returned by the server (&#x60;BannedUserItem&#x60; uses string). | [optional] 

## Methods

### NewBannedUser

`func NewBannedUser() *BannedUser`

NewBannedUser instantiates a new BannedUser object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBannedUserWithDefaults

`func NewBannedUserWithDefaults() *BannedUser`

NewBannedUserWithDefaults instantiates a new BannedUser object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *BannedUser) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *BannedUser) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *BannedUser) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *BannedUser) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetBanExpiresAt

`func (o *BannedUser) GetBanExpiresAt() string`

GetBanExpiresAt returns the BanExpiresAt field if non-nil, zero value otherwise.

### GetBanExpiresAtOk

`func (o *BannedUser) GetBanExpiresAtOk() (*string, bool)`

GetBanExpiresAtOk returns a tuple with the BanExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBanExpiresAt

`func (o *BannedUser) SetBanExpiresAt(v string)`

SetBanExpiresAt sets BanExpiresAt field to given value.

### HasBanExpiresAt

`func (o *BannedUser) HasBanExpiresAt() bool`

HasBanExpiresAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



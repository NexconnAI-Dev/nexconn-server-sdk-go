# AccessTokenExpireRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserIds** | **[]string** |  | 
**ExpiresAt** | **int64** | Expiration timestamp in milliseconds. | 

## Methods

### NewAccessTokenExpireRequest

`func NewAccessTokenExpireRequest(userIds []string, expiresAt int64, ) *AccessTokenExpireRequest`

NewAccessTokenExpireRequest instantiates a new AccessTokenExpireRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAccessTokenExpireRequestWithDefaults

`func NewAccessTokenExpireRequestWithDefaults() *AccessTokenExpireRequest`

NewAccessTokenExpireRequestWithDefaults instantiates a new AccessTokenExpireRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserIds

`func (o *AccessTokenExpireRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *AccessTokenExpireRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *AccessTokenExpireRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetExpiresAt

`func (o *AccessTokenExpireRequest) GetExpiresAt() int64`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *AccessTokenExpireRequest) GetExpiresAtOk() (*int64, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *AccessTokenExpireRequest) SetExpiresAt(v int64)`

SetExpiresAt sets ExpiresAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



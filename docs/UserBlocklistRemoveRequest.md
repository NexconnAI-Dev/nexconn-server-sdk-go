# UserBlocklistRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**BlockedUserIds** | **[]string** |  | 

## Methods

### NewUserBlocklistRemoveRequest

`func NewUserBlocklistRemoveRequest(userId string, blockedUserIds []string, ) *UserBlocklistRemoveRequest`

NewUserBlocklistRemoveRequest instantiates a new UserBlocklistRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBlocklistRemoveRequestWithDefaults

`func NewUserBlocklistRemoveRequestWithDefaults() *UserBlocklistRemoveRequest`

NewUserBlocklistRemoveRequestWithDefaults instantiates a new UserBlocklistRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserBlocklistRemoveRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserBlocklistRemoveRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserBlocklistRemoveRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetBlockedUserIds

`func (o *UserBlocklistRemoveRequest) GetBlockedUserIds() []string`

GetBlockedUserIds returns the BlockedUserIds field if non-nil, zero value otherwise.

### GetBlockedUserIdsOk

`func (o *UserBlocklistRemoveRequest) GetBlockedUserIdsOk() (*[]string, bool)`

GetBlockedUserIdsOk returns a tuple with the BlockedUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBlockedUserIds

`func (o *UserBlocklistRemoveRequest) SetBlockedUserIds(v []string)`

SetBlockedUserIds sets BlockedUserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



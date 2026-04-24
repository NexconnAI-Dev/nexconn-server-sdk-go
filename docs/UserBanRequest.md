# UserBanRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserIds** | **[]string** |  | 
**DurationMinutes** | **int32** |  | 

## Methods

### NewUserBanRequest

`func NewUserBanRequest(userIds []string, durationMinutes int32, ) *UserBanRequest`

NewUserBanRequest instantiates a new UserBanRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBanRequestWithDefaults

`func NewUserBanRequestWithDefaults() *UserBanRequest`

NewUserBanRequestWithDefaults instantiates a new UserBanRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserIds

`func (o *UserBanRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *UserBanRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *UserBanRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetDurationMinutes

`func (o *UserBanRequest) GetDurationMinutes() int32`

GetDurationMinutes returns the DurationMinutes field if non-nil, zero value otherwise.

### GetDurationMinutesOk

`func (o *UserBanRequest) GetDurationMinutesOk() (*int32, bool)`

GetDurationMinutesOk returns a tuple with the DurationMinutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDurationMinutes

`func (o *UserBanRequest) SetDurationMinutes(v int32)`

SetDurationMinutes sets DurationMinutes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



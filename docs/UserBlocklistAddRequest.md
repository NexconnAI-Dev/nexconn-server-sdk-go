# UserBlocklistAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TargetUserIds** | **[]string** |  | 

## Methods

### NewUserBlocklistAddRequest

`func NewUserBlocklistAddRequest(userId string, targetUserIds []string, ) *UserBlocklistAddRequest`

NewUserBlocklistAddRequest instantiates a new UserBlocklistAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBlocklistAddRequestWithDefaults

`func NewUserBlocklistAddRequestWithDefaults() *UserBlocklistAddRequest`

NewUserBlocklistAddRequestWithDefaults instantiates a new UserBlocklistAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserBlocklistAddRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserBlocklistAddRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserBlocklistAddRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTargetUserIds

`func (o *UserBlocklistAddRequest) GetTargetUserIds() []string`

GetTargetUserIds returns the TargetUserIds field if non-nil, zero value otherwise.

### GetTargetUserIdsOk

`func (o *UserBlocklistAddRequest) GetTargetUserIdsOk() (*[]string, bool)`

GetTargetUserIdsOk returns a tuple with the TargetUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetUserIds

`func (o *UserBlocklistAddRequest) SetTargetUserIds(v []string)`

SetTargetUserIds sets TargetUserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



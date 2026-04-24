# FriendRelationshipGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TargetIds** | **[]string** |  | 

## Methods

### NewFriendRelationshipGetRequest

`func NewFriendRelationshipGetRequest(userId string, targetIds []string, ) *FriendRelationshipGetRequest`

NewFriendRelationshipGetRequest instantiates a new FriendRelationshipGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendRelationshipGetRequestWithDefaults

`func NewFriendRelationshipGetRequestWithDefaults() *FriendRelationshipGetRequest`

NewFriendRelationshipGetRequestWithDefaults instantiates a new FriendRelationshipGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendRelationshipGetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendRelationshipGetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendRelationshipGetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTargetIds

`func (o *FriendRelationshipGetRequest) GetTargetIds() []string`

GetTargetIds returns the TargetIds field if non-nil, zero value otherwise.

### GetTargetIdsOk

`func (o *FriendRelationshipGetRequest) GetTargetIdsOk() (*[]string, bool)`

GetTargetIdsOk returns a tuple with the TargetIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetIds

`func (o *FriendRelationshipGetRequest) SetTargetIds(v []string)`

SetTargetIds sets TargetIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FriendAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TargetId** | **string** |  | 
**Action** | Pointer to **int32** | &#x60;1&#x60; means add with verification and &#x60;2&#x60; means add directly. | [optional] 
**Extra** | Pointer to **string** |  | [optional] 

## Methods

### NewFriendAddRequest

`func NewFriendAddRequest(userId string, targetId string, ) *FriendAddRequest`

NewFriendAddRequest instantiates a new FriendAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendAddRequestWithDefaults

`func NewFriendAddRequestWithDefaults() *FriendAddRequest`

NewFriendAddRequestWithDefaults instantiates a new FriendAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendAddRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendAddRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendAddRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTargetId

`func (o *FriendAddRequest) GetTargetId() string`

GetTargetId returns the TargetId field if non-nil, zero value otherwise.

### GetTargetIdOk

`func (o *FriendAddRequest) GetTargetIdOk() (*string, bool)`

GetTargetIdOk returns a tuple with the TargetId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetId

`func (o *FriendAddRequest) SetTargetId(v string)`

SetTargetId sets TargetId field to given value.


### GetAction

`func (o *FriendAddRequest) GetAction() int32`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *FriendAddRequest) GetActionOk() (*int32, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *FriendAddRequest) SetAction(v int32)`

SetAction sets Action field to given value.

### HasAction

`func (o *FriendAddRequest) HasAction() bool`

HasAction returns a boolean if a field has been set.

### GetExtra

`func (o *FriendAddRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *FriendAddRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *FriendAddRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *FriendAddRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



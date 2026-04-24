# FriendRelationshipItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** |  | [optional] 
**Result** | Pointer to **int32** | Friend relationship result defined by the source API. &#x60;1&#x60; means both users are not friends, &#x60;2&#x60; and &#x60;3&#x60; are reserved, and &#x60;4&#x60; means the friendship is mutual.  | [optional] 

## Methods

### NewFriendRelationshipItem

`func NewFriendRelationshipItem() *FriendRelationshipItem`

NewFriendRelationshipItem instantiates a new FriendRelationshipItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendRelationshipItemWithDefaults

`func NewFriendRelationshipItemWithDefaults() *FriendRelationshipItem`

NewFriendRelationshipItemWithDefaults instantiates a new FriendRelationshipItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendRelationshipItem) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendRelationshipItem) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendRelationshipItem) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *FriendRelationshipItem) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetResult

`func (o *FriendRelationshipItem) GetResult() int32`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *FriendRelationshipItem) GetResultOk() (*int32, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *FriendRelationshipItem) SetResult(v int32)`

SetResult sets Result field to given value.

### HasResult

`func (o *FriendRelationshipItem) HasResult() bool`

HasResult returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



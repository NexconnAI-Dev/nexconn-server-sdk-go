# FriendListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** |  | [optional] 
**TotalCount** | Pointer to **int32** |  | [optional] 
**Friends** | Pointer to [**[]FriendItem**](FriendItem.md) |  | [optional] 

## Methods

### NewFriendListResponseResult

`func NewFriendListResponseResult() *FriendListResponseResult`

NewFriendListResponseResult instantiates a new FriendListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendListResponseResultWithDefaults

`func NewFriendListResponseResultWithDefaults() *FriendListResponseResult`

NewFriendListResponseResultWithDefaults instantiates a new FriendListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *FriendListResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *FriendListResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *FriendListResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *FriendListResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetTotalCount

`func (o *FriendListResponseResult) GetTotalCount() int32`

GetTotalCount returns the TotalCount field if non-nil, zero value otherwise.

### GetTotalCountOk

`func (o *FriendListResponseResult) GetTotalCountOk() (*int32, bool)`

GetTotalCountOk returns a tuple with the TotalCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotalCount

`func (o *FriendListResponseResult) SetTotalCount(v int32)`

SetTotalCount sets TotalCount field to given value.

### HasTotalCount

`func (o *FriendListResponseResult) HasTotalCount() bool`

HasTotalCount returns a boolean if a field has been set.

### GetFriends

`func (o *FriendListResponseResult) GetFriends() []FriendItem`

GetFriends returns the Friends field if non-nil, zero value otherwise.

### GetFriendsOk

`func (o *FriendListResponseResult) GetFriendsOk() (*[]FriendItem, bool)`

GetFriendsOk returns a tuple with the Friends field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFriends

`func (o *FriendListResponseResult) SetFriends(v []FriendItem)`

SetFriends sets Friends field to given value.

### HasFriends

`func (o *FriendListResponseResult) HasFriends() bool`

HasFriends returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



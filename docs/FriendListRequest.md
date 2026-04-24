# FriendListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**PageToken** | Pointer to **string** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] [default to 50]
**Order** | Pointer to **int32** | &#x60;0&#x60; for ascending order and &#x60;1&#x60; for descending order. | [optional] 

## Methods

### NewFriendListRequest

`func NewFriendListRequest(userId string, ) *FriendListRequest`

NewFriendListRequest instantiates a new FriendListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewFriendListRequestWithDefaults

`func NewFriendListRequestWithDefaults() *FriendListRequest`

NewFriendListRequestWithDefaults instantiates a new FriendListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *FriendListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *FriendListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *FriendListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetPageToken

`func (o *FriendListRequest) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *FriendListRequest) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *FriendListRequest) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *FriendListRequest) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetPageSize

`func (o *FriendListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *FriendListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *FriendListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *FriendListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *FriendListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *FriendListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *FriendListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *FriendListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



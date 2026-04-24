# GroupChannelJoinedListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** | User ID whose joined groups should be listed. | 
**Role** | Pointer to **int32** | Role filter. &#x60;0&#x60; all roles, &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] 
**PageToken** | Pointer to **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional] 
**PageSize** | Pointer to **int32** | Number of groups to return per page. The official default is 50 and the maximum is 100. | [optional] 
**Order** | Pointer to **int32** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional] 

## Methods

### NewGroupChannelJoinedListRequest

`func NewGroupChannelJoinedListRequest(userId string, ) *GroupChannelJoinedListRequest`

NewGroupChannelJoinedListRequest instantiates a new GroupChannelJoinedListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelJoinedListRequestWithDefaults

`func NewGroupChannelJoinedListRequestWithDefaults() *GroupChannelJoinedListRequest`

NewGroupChannelJoinedListRequestWithDefaults instantiates a new GroupChannelJoinedListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *GroupChannelJoinedListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelJoinedListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelJoinedListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetRole

`func (o *GroupChannelJoinedListRequest) GetRole() int32`

GetRole returns the Role field if non-nil, zero value otherwise.

### GetRoleOk

`func (o *GroupChannelJoinedListRequest) GetRoleOk() (*int32, bool)`

GetRoleOk returns a tuple with the Role field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRole

`func (o *GroupChannelJoinedListRequest) SetRole(v int32)`

SetRole sets Role field to given value.

### HasRole

`func (o *GroupChannelJoinedListRequest) HasRole() bool`

HasRole returns a boolean if a field has been set.

### GetPageToken

`func (o *GroupChannelJoinedListRequest) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelJoinedListRequest) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelJoinedListRequest) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelJoinedListRequest) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetPageSize

`func (o *GroupChannelJoinedListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *GroupChannelJoinedListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *GroupChannelJoinedListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *GroupChannelJoinedListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *GroupChannelJoinedListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *GroupChannelJoinedListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *GroupChannelJoinedListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *GroupChannelJoinedListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



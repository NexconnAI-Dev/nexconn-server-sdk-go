# GroupChannelMemberListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | Group channel ID. | 
**MemberRole** | Pointer to **int32** | Member role filter. &#x60;0&#x60; all members, &#x60;1&#x60; regular members, &#x60;2&#x60; admins, &#x60;3&#x60; owner. | [optional] 
**PageToken** | Pointer to **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional] 
**PageSize** | Pointer to **int32** | Number of members to return per page. The official default is 50 and the maximum is 100. | [optional] 
**Order** | Pointer to **int32** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional] 

## Methods

### NewGroupChannelMemberListRequest

`func NewGroupChannelMemberListRequest(channelId string, ) *GroupChannelMemberListRequest`

NewGroupChannelMemberListRequest instantiates a new GroupChannelMemberListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberListRequestWithDefaults

`func NewGroupChannelMemberListRequestWithDefaults() *GroupChannelMemberListRequest`

NewGroupChannelMemberListRequestWithDefaults instantiates a new GroupChannelMemberListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelMemberListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelMemberListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelMemberListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetMemberRole

`func (o *GroupChannelMemberListRequest) GetMemberRole() int32`

GetMemberRole returns the MemberRole field if non-nil, zero value otherwise.

### GetMemberRoleOk

`func (o *GroupChannelMemberListRequest) GetMemberRoleOk() (*int32, bool)`

GetMemberRoleOk returns a tuple with the MemberRole field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMemberRole

`func (o *GroupChannelMemberListRequest) SetMemberRole(v int32)`

SetMemberRole sets MemberRole field to given value.

### HasMemberRole

`func (o *GroupChannelMemberListRequest) HasMemberRole() bool`

HasMemberRole returns a boolean if a field has been set.

### GetPageToken

`func (o *GroupChannelMemberListRequest) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelMemberListRequest) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelMemberListRequest) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelMemberListRequest) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetPageSize

`func (o *GroupChannelMemberListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *GroupChannelMemberListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *GroupChannelMemberListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *GroupChannelMemberListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *GroupChannelMemberListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *GroupChannelMemberListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *GroupChannelMemberListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *GroupChannelMemberListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



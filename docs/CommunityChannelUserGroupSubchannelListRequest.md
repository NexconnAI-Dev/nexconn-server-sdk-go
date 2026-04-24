# CommunityChannelUserGroupSubchannelListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserGroupId** | **string** |  | 
**Page** | Pointer to **int32** |  | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 10]

## Methods

### NewCommunityChannelUserGroupSubchannelListRequest

`func NewCommunityChannelUserGroupSubchannelListRequest(channelId string, userGroupId string, ) *CommunityChannelUserGroupSubchannelListRequest`

NewCommunityChannelUserGroupSubchannelListRequest instantiates a new CommunityChannelUserGroupSubchannelListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelUserGroupSubchannelListRequestWithDefaults

`func NewCommunityChannelUserGroupSubchannelListRequestWithDefaults() *CommunityChannelUserGroupSubchannelListRequest`

NewCommunityChannelUserGroupSubchannelListRequestWithDefaults instantiates a new CommunityChannelUserGroupSubchannelListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelUserGroupSubchannelListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserGroupId

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetUserGroupId() string`

GetUserGroupId returns the UserGroupId field if non-nil, zero value otherwise.

### GetUserGroupIdOk

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetUserGroupIdOk() (*string, bool)`

GetUserGroupIdOk returns a tuple with the UserGroupId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserGroupId

`func (o *CommunityChannelUserGroupSubchannelListRequest) SetUserGroupId(v string)`

SetUserGroupId sets UserGroupId field to given value.


### GetPage

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityChannelUserGroupSubchannelListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityChannelUserGroupSubchannelListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityChannelUserGroupSubchannelListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityChannelUserGroupSubchannelListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityChannelUserGroupSubchannelListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



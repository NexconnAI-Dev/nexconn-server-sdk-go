# CommunityChannelUserGroupAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserGroups** | [**[]CommunityChannelUserGroupItem**](CommunityChannelUserGroupItem.md) |  | 

## Methods

### NewCommunityChannelUserGroupAddRequest

`func NewCommunityChannelUserGroupAddRequest(channelId string, userGroups []CommunityChannelUserGroupItem, ) *CommunityChannelUserGroupAddRequest`

NewCommunityChannelUserGroupAddRequest instantiates a new CommunityChannelUserGroupAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelUserGroupAddRequestWithDefaults

`func NewCommunityChannelUserGroupAddRequestWithDefaults() *CommunityChannelUserGroupAddRequest`

NewCommunityChannelUserGroupAddRequestWithDefaults instantiates a new CommunityChannelUserGroupAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelUserGroupAddRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelUserGroupAddRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelUserGroupAddRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserGroups

`func (o *CommunityChannelUserGroupAddRequest) GetUserGroups() []CommunityChannelUserGroupItem`

GetUserGroups returns the UserGroups field if non-nil, zero value otherwise.

### GetUserGroupsOk

`func (o *CommunityChannelUserGroupAddRequest) GetUserGroupsOk() (*[]CommunityChannelUserGroupItem, bool)`

GetUserGroupsOk returns a tuple with the UserGroups field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserGroups

`func (o *CommunityChannelUserGroupAddRequest) SetUserGroups(v []CommunityChannelUserGroupItem)`

SetUserGroups sets UserGroups field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



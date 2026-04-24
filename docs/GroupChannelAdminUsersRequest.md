# GroupChannelAdminUsersRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserIds** | **[]string** |  | 

## Methods

### NewGroupChannelAdminUsersRequest

`func NewGroupChannelAdminUsersRequest(channelId string, userIds []string, ) *GroupChannelAdminUsersRequest`

NewGroupChannelAdminUsersRequest instantiates a new GroupChannelAdminUsersRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelAdminUsersRequestWithDefaults

`func NewGroupChannelAdminUsersRequestWithDefaults() *GroupChannelAdminUsersRequest`

NewGroupChannelAdminUsersRequestWithDefaults instantiates a new GroupChannelAdminUsersRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelAdminUsersRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelAdminUsersRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelAdminUsersRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserIds

`func (o *GroupChannelAdminUsersRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *GroupChannelAdminUsersRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *GroupChannelAdminUsersRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



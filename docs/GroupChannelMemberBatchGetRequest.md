# GroupChannelMemberBatchGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserIds** | **[]string** |  | 

## Methods

### NewGroupChannelMemberBatchGetRequest

`func NewGroupChannelMemberBatchGetRequest(channelId string, userIds []string, ) *GroupChannelMemberBatchGetRequest`

NewGroupChannelMemberBatchGetRequest instantiates a new GroupChannelMemberBatchGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberBatchGetRequestWithDefaults

`func NewGroupChannelMemberBatchGetRequestWithDefaults() *GroupChannelMemberBatchGetRequest`

NewGroupChannelMemberBatchGetRequestWithDefaults instantiates a new GroupChannelMemberBatchGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelMemberBatchGetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelMemberBatchGetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelMemberBatchGetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserIds

`func (o *GroupChannelMemberBatchGetRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *GroupChannelMemberBatchGetRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *GroupChannelMemberBatchGetRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



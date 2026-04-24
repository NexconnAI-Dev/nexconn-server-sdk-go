# GroupChannelUserMuteListRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Optional. When omitted, the operation applies to all group channels according to the PDF. | [optional] 
**UserIds** | **[]string** |  | 

## Methods

### NewGroupChannelUserMuteListRemoveRequest

`func NewGroupChannelUserMuteListRemoveRequest(userIds []string, ) *GroupChannelUserMuteListRemoveRequest`

NewGroupChannelUserMuteListRemoveRequest instantiates a new GroupChannelUserMuteListRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelUserMuteListRemoveRequestWithDefaults

`func NewGroupChannelUserMuteListRemoveRequestWithDefaults() *GroupChannelUserMuteListRemoveRequest`

NewGroupChannelUserMuteListRemoveRequestWithDefaults instantiates a new GroupChannelUserMuteListRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelUserMuteListRemoveRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelUserMuteListRemoveRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelUserMuteListRemoveRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelUserMuteListRemoveRequest) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetUserIds

`func (o *GroupChannelUserMuteListRemoveRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *GroupChannelUserMuteListRemoveRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *GroupChannelUserMuteListRemoveRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



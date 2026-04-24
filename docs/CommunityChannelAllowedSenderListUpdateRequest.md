# CommunityChannelAllowedSenderListUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**UserIds** | **[]string** |  | 

## Methods

### NewCommunityChannelAllowedSenderListUpdateRequest

`func NewCommunityChannelAllowedSenderListUpdateRequest(channelId string, userIds []string, ) *CommunityChannelAllowedSenderListUpdateRequest`

NewCommunityChannelAllowedSenderListUpdateRequest instantiates a new CommunityChannelAllowedSenderListUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelAllowedSenderListUpdateRequestWithDefaults

`func NewCommunityChannelAllowedSenderListUpdateRequestWithDefaults() *CommunityChannelAllowedSenderListUpdateRequest`

NewCommunityChannelAllowedSenderListUpdateRequestWithDefaults instantiates a new CommunityChannelAllowedSenderListUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelAllowedSenderListUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelAllowedSenderListUpdateRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelAllowedSenderListUpdateRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetUserIds

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *CommunityChannelAllowedSenderListUpdateRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *CommunityChannelAllowedSenderListUpdateRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



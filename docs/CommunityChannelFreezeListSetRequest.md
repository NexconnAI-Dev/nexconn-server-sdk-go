# CommunityChannelFreezeListSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**Status** | **bool** | Freeze status for the community channel or subchannel. | 

## Methods

### NewCommunityChannelFreezeListSetRequest

`func NewCommunityChannelFreezeListSetRequest(channelId string, status bool, ) *CommunityChannelFreezeListSetRequest`

NewCommunityChannelFreezeListSetRequest instantiates a new CommunityChannelFreezeListSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelFreezeListSetRequestWithDefaults

`func NewCommunityChannelFreezeListSetRequestWithDefaults() *CommunityChannelFreezeListSetRequest`

NewCommunityChannelFreezeListSetRequestWithDefaults instantiates a new CommunityChannelFreezeListSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelFreezeListSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelFreezeListSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelFreezeListSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelFreezeListSetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelFreezeListSetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelFreezeListSetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelFreezeListSetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetStatus

`func (o *CommunityChannelFreezeListSetRequest) GetStatus() bool`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CommunityChannelFreezeListSetRequest) GetStatusOk() (*bool, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CommunityChannelFreezeListSetRequest) SetStatus(v bool)`

SetStatus sets Status field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



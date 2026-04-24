# CommunityChannelHistoryMessageListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | **string** |  | 
**StartAt** | **int64** |  | 
**EndAt** | **int64** |  | 
**FromUserId** | Pointer to **string** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] [default to 20]

## Methods

### NewCommunityChannelHistoryMessageListRequest

`func NewCommunityChannelHistoryMessageListRequest(channelId string, subchannelId string, startAt int64, endAt int64, ) *CommunityChannelHistoryMessageListRequest`

NewCommunityChannelHistoryMessageListRequest instantiates a new CommunityChannelHistoryMessageListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelHistoryMessageListRequestWithDefaults

`func NewCommunityChannelHistoryMessageListRequestWithDefaults() *CommunityChannelHistoryMessageListRequest`

NewCommunityChannelHistoryMessageListRequestWithDefaults instantiates a new CommunityChannelHistoryMessageListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelHistoryMessageListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelHistoryMessageListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelHistoryMessageListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelHistoryMessageListRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelHistoryMessageListRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelHistoryMessageListRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.


### GetStartAt

`func (o *CommunityChannelHistoryMessageListRequest) GetStartAt() int64`

GetStartAt returns the StartAt field if non-nil, zero value otherwise.

### GetStartAtOk

`func (o *CommunityChannelHistoryMessageListRequest) GetStartAtOk() (*int64, bool)`

GetStartAtOk returns a tuple with the StartAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartAt

`func (o *CommunityChannelHistoryMessageListRequest) SetStartAt(v int64)`

SetStartAt sets StartAt field to given value.


### GetEndAt

`func (o *CommunityChannelHistoryMessageListRequest) GetEndAt() int64`

GetEndAt returns the EndAt field if non-nil, zero value otherwise.

### GetEndAtOk

`func (o *CommunityChannelHistoryMessageListRequest) GetEndAtOk() (*int64, bool)`

GetEndAtOk returns a tuple with the EndAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndAt

`func (o *CommunityChannelHistoryMessageListRequest) SetEndAt(v int64)`

SetEndAt sets EndAt field to given value.


### GetFromUserId

`func (o *CommunityChannelHistoryMessageListRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *CommunityChannelHistoryMessageListRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *CommunityChannelHistoryMessageListRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.

### HasFromUserId

`func (o *CommunityChannelHistoryMessageListRequest) HasFromUserId() bool`

HasFromUserId returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityChannelHistoryMessageListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityChannelHistoryMessageListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityChannelHistoryMessageListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityChannelHistoryMessageListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



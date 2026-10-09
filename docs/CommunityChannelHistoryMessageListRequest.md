# CommunityChannelHistoryMessageListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | Community channel ID. | 
**SubchannelId** | Pointer to **string** | Optional community subchannel ID. When omitted, messages from the whole community channel are queried. | [optional] 
**UserId** | **string** | User ID of the community-channel participant. | 
**StartAt** | **int64** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. | 
**EndAt** | **int64** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. | 
**PageSize** | Pointer to **int32** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**IncludeStart** | **bool** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. | 

## Methods

### NewCommunityChannelHistoryMessageListRequest

`func NewCommunityChannelHistoryMessageListRequest(channelId string, userId string, startAt int64, endAt int64, includeStart bool, ) *CommunityChannelHistoryMessageListRequest`

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

### HasSubchannelId

`func (o *CommunityChannelHistoryMessageListRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetUserId

`func (o *CommunityChannelHistoryMessageListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityChannelHistoryMessageListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityChannelHistoryMessageListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


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

### GetIncludeStart

`func (o *CommunityChannelHistoryMessageListRequest) GetIncludeStart() bool`

GetIncludeStart returns the IncludeStart field if non-nil, zero value otherwise.

### GetIncludeStartOk

`func (o *CommunityChannelHistoryMessageListRequest) GetIncludeStartOk() (*bool, bool)`

GetIncludeStartOk returns a tuple with the IncludeStart field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIncludeStart

`func (o *CommunityChannelHistoryMessageListRequest) SetIncludeStart(v bool)`

SetIncludeStart sets IncludeStart field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



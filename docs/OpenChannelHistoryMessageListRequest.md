# OpenChannelHistoryMessageListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** | User ID of the open-channel participant. | 
**ChannelId** | **string** | Open channel ID. | 
**StartAt** | **int64** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. | 
**EndAt** | **int64** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. | 
**PageSize** | Pointer to **int32** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**IncludeStart** | **bool** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. | 

## Methods

### NewOpenChannelHistoryMessageListRequest

`func NewOpenChannelHistoryMessageListRequest(userId string, channelId string, startAt int64, endAt int64, includeStart bool, ) *OpenChannelHistoryMessageListRequest`

NewOpenChannelHistoryMessageListRequest instantiates a new OpenChannelHistoryMessageListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelHistoryMessageListRequestWithDefaults

`func NewOpenChannelHistoryMessageListRequestWithDefaults() *OpenChannelHistoryMessageListRequest`

NewOpenChannelHistoryMessageListRequestWithDefaults instantiates a new OpenChannelHistoryMessageListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *OpenChannelHistoryMessageListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *OpenChannelHistoryMessageListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *OpenChannelHistoryMessageListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelId

`func (o *OpenChannelHistoryMessageListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelHistoryMessageListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelHistoryMessageListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetStartAt

`func (o *OpenChannelHistoryMessageListRequest) GetStartAt() int64`

GetStartAt returns the StartAt field if non-nil, zero value otherwise.

### GetStartAtOk

`func (o *OpenChannelHistoryMessageListRequest) GetStartAtOk() (*int64, bool)`

GetStartAtOk returns a tuple with the StartAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartAt

`func (o *OpenChannelHistoryMessageListRequest) SetStartAt(v int64)`

SetStartAt sets StartAt field to given value.


### GetEndAt

`func (o *OpenChannelHistoryMessageListRequest) GetEndAt() int64`

GetEndAt returns the EndAt field if non-nil, zero value otherwise.

### GetEndAtOk

`func (o *OpenChannelHistoryMessageListRequest) GetEndAtOk() (*int64, bool)`

GetEndAtOk returns a tuple with the EndAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndAt

`func (o *OpenChannelHistoryMessageListRequest) SetEndAt(v int64)`

SetEndAt sets EndAt field to given value.


### GetPageSize

`func (o *OpenChannelHistoryMessageListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *OpenChannelHistoryMessageListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *OpenChannelHistoryMessageListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *OpenChannelHistoryMessageListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetIncludeStart

`func (o *OpenChannelHistoryMessageListRequest) GetIncludeStart() bool`

GetIncludeStart returns the IncludeStart field if non-nil, zero value otherwise.

### GetIncludeStartOk

`func (o *OpenChannelHistoryMessageListRequest) GetIncludeStartOk() (*bool, bool)`

GetIncludeStartOk returns a tuple with the IncludeStart field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIncludeStart

`func (o *OpenChannelHistoryMessageListRequest) SetIncludeStart(v bool)`

SetIncludeStart sets IncludeStart field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



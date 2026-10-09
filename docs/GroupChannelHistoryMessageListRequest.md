# GroupChannelHistoryMessageListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** | User ID of the group-channel participant. | 
**ChannelId** | **string** | Group channel ID. | 
**StartAt** | **int64** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. | 
**EndAt** | **int64** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. | 
**PageSize** | Pointer to **int32** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**IncludeStart** | **bool** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. | 

## Methods

### NewGroupChannelHistoryMessageListRequest

`func NewGroupChannelHistoryMessageListRequest(userId string, channelId string, startAt int64, endAt int64, includeStart bool, ) *GroupChannelHistoryMessageListRequest`

NewGroupChannelHistoryMessageListRequest instantiates a new GroupChannelHistoryMessageListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelHistoryMessageListRequestWithDefaults

`func NewGroupChannelHistoryMessageListRequestWithDefaults() *GroupChannelHistoryMessageListRequest`

NewGroupChannelHistoryMessageListRequestWithDefaults instantiates a new GroupChannelHistoryMessageListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *GroupChannelHistoryMessageListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *GroupChannelHistoryMessageListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *GroupChannelHistoryMessageListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelId

`func (o *GroupChannelHistoryMessageListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelHistoryMessageListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelHistoryMessageListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetStartAt

`func (o *GroupChannelHistoryMessageListRequest) GetStartAt() int64`

GetStartAt returns the StartAt field if non-nil, zero value otherwise.

### GetStartAtOk

`func (o *GroupChannelHistoryMessageListRequest) GetStartAtOk() (*int64, bool)`

GetStartAtOk returns a tuple with the StartAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartAt

`func (o *GroupChannelHistoryMessageListRequest) SetStartAt(v int64)`

SetStartAt sets StartAt field to given value.


### GetEndAt

`func (o *GroupChannelHistoryMessageListRequest) GetEndAt() int64`

GetEndAt returns the EndAt field if non-nil, zero value otherwise.

### GetEndAtOk

`func (o *GroupChannelHistoryMessageListRequest) GetEndAtOk() (*int64, bool)`

GetEndAtOk returns a tuple with the EndAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndAt

`func (o *GroupChannelHistoryMessageListRequest) SetEndAt(v int64)`

SetEndAt sets EndAt field to given value.


### GetPageSize

`func (o *GroupChannelHistoryMessageListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *GroupChannelHistoryMessageListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *GroupChannelHistoryMessageListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *GroupChannelHistoryMessageListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetIncludeStart

`func (o *GroupChannelHistoryMessageListRequest) GetIncludeStart() bool`

GetIncludeStart returns the IncludeStart field if non-nil, zero value otherwise.

### GetIncludeStartOk

`func (o *GroupChannelHistoryMessageListRequest) GetIncludeStartOk() (*bool, bool)`

GetIncludeStartOk returns a tuple with the IncludeStart field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIncludeStart

`func (o *GroupChannelHistoryMessageListRequest) SetIncludeStart(v bool)`

SetIncludeStart sets IncludeStart field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ChannelMessageHistoryDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | **int32** | Channel type. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, and &#x60;6&#x60; system (&#x60;HistoryCleanInput&#x60;). | 
**FromUserId** | **string** | User whose server-side history is operated on. For open channels, this is the operator ID. | 
**ChannelId** | **string** | Target channel ID (&#x60;targetId&#x60; / conversation target). | 
**SentAt** | Pointer to **string** | Optional cutoff (&#x60;msgTimestamp&#x60;). Serialized as string in &#x60;HistoryCleanInput&#x60;. | [optional] 

## Methods

### NewChannelMessageHistoryDeleteRequest

`func NewChannelMessageHistoryDeleteRequest(channelType int32, fromUserId string, channelId string, ) *ChannelMessageHistoryDeleteRequest`

NewChannelMessageHistoryDeleteRequest instantiates a new ChannelMessageHistoryDeleteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelMessageHistoryDeleteRequestWithDefaults

`func NewChannelMessageHistoryDeleteRequestWithDefaults() *ChannelMessageHistoryDeleteRequest`

NewChannelMessageHistoryDeleteRequestWithDefaults instantiates a new ChannelMessageHistoryDeleteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelType

`func (o *ChannelMessageHistoryDeleteRequest) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelMessageHistoryDeleteRequest) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelMessageHistoryDeleteRequest) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.


### GetFromUserId

`func (o *ChannelMessageHistoryDeleteRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *ChannelMessageHistoryDeleteRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *ChannelMessageHistoryDeleteRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetChannelId

`func (o *ChannelMessageHistoryDeleteRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelMessageHistoryDeleteRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelMessageHistoryDeleteRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSentAt

`func (o *ChannelMessageHistoryDeleteRequest) GetSentAt() string`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *ChannelMessageHistoryDeleteRequest) GetSentAtOk() (*string, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *ChannelMessageHistoryDeleteRequest) SetSentAt(v string)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *ChannelMessageHistoryDeleteRequest) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



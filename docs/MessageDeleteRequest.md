# MessageDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID of the original message that is being deleted. | 
**ChannelType** | **int32** | Channel type of the original message. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, &#x60;6&#x60; system, and &#x60;10&#x60; community. | 
**ChannelId** | **string** | Target identifier of the original message. Depending on &#x60;channelType&#x60;, this can be a user ID, group ID, open channel ID, community channel ID, or system target ID. | 
**SubchannelId** | Pointer to **string** | Community subchannel ID. Required only when deleting a community-channel message that was sent to a specific subchannel. | [optional] 
**MessageId** | **string** | Unique message ID to delete. This corresponds to the message UID returned by send or routing services. | 
**SentAt** | Pointer to **int64** | Send timestamp of the original message in milliseconds. Providing it helps the service locate the original message precisely. | [optional] 
**IsAdmin** | Pointer to **int32** | Whether the deletion is performed as an admin operation. &#x60;1&#x60; shows an admin recall indicator and &#x60;0&#x60; performs a normal sender recall. | [optional] 
**DisablePush** | Pointer to **bool** | Whether to suppress push notifications for the recall event. Not supported for open channels or community channels. | [optional] 
**Extra** | Pointer to **string** | Custom extension data carried with the recall operation. Not supported for community channels. | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep the recall operation from updating the channel&#39;s last-message preview. | [optional] 

## Methods

### NewMessageDeleteRequest

`func NewMessageDeleteRequest(fromUserId string, channelType int32, channelId string, messageId string, ) *MessageDeleteRequest`

NewMessageDeleteRequest instantiates a new MessageDeleteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMessageDeleteRequestWithDefaults

`func NewMessageDeleteRequestWithDefaults() *MessageDeleteRequest`

NewMessageDeleteRequestWithDefaults instantiates a new MessageDeleteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *MessageDeleteRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *MessageDeleteRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *MessageDeleteRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetChannelType

`func (o *MessageDeleteRequest) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *MessageDeleteRequest) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *MessageDeleteRequest) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.


### GetChannelId

`func (o *MessageDeleteRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *MessageDeleteRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *MessageDeleteRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *MessageDeleteRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *MessageDeleteRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *MessageDeleteRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *MessageDeleteRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetMessageId

`func (o *MessageDeleteRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *MessageDeleteRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *MessageDeleteRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetSentAt

`func (o *MessageDeleteRequest) GetSentAt() int64`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *MessageDeleteRequest) GetSentAtOk() (*int64, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *MessageDeleteRequest) SetSentAt(v int64)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *MessageDeleteRequest) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.

### GetIsAdmin

`func (o *MessageDeleteRequest) GetIsAdmin() int32`

GetIsAdmin returns the IsAdmin field if non-nil, zero value otherwise.

### GetIsAdminOk

`func (o *MessageDeleteRequest) GetIsAdminOk() (*int32, bool)`

GetIsAdminOk returns a tuple with the IsAdmin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsAdmin

`func (o *MessageDeleteRequest) SetIsAdmin(v int32)`

SetIsAdmin sets IsAdmin field to given value.

### HasIsAdmin

`func (o *MessageDeleteRequest) HasIsAdmin() bool`

HasIsAdmin returns a boolean if a field has been set.

### GetDisablePush

`func (o *MessageDeleteRequest) GetDisablePush() bool`

GetDisablePush returns the DisablePush field if non-nil, zero value otherwise.

### GetDisablePushOk

`func (o *MessageDeleteRequest) GetDisablePushOk() (*bool, bool)`

GetDisablePushOk returns a tuple with the DisablePush field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisablePush

`func (o *MessageDeleteRequest) SetDisablePush(v bool)`

SetDisablePush sets DisablePush field to given value.

### HasDisablePush

`func (o *MessageDeleteRequest) HasDisablePush() bool`

HasDisablePush returns a boolean if a field has been set.

### GetExtra

`func (o *MessageDeleteRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *MessageDeleteRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *MessageDeleteRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *MessageDeleteRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *MessageDeleteRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *MessageDeleteRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *MessageDeleteRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *MessageDeleteRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



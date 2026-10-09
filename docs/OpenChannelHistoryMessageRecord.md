# OpenChannelHistoryMessageRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Channel identifier of the stored message. | [optional] 
**FromUserId** | Pointer to **string** | Sender user ID of the stored message. | [optional] 
**MessageId** | Pointer to **string** | Unique message ID. | [optional] 
**SentAt** | Pointer to **int64** | Message send timestamp in milliseconds. | [optional] 
**MessageType** | Pointer to **string** | Message type of the stored message. | [optional] 
**Content** | Pointer to **string** | Raw message content payload as stored by the service. | [optional] 
**Quote** | Pointer to **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional] 

## Methods

### NewOpenChannelHistoryMessageRecord

`func NewOpenChannelHistoryMessageRecord() *OpenChannelHistoryMessageRecord`

NewOpenChannelHistoryMessageRecord instantiates a new OpenChannelHistoryMessageRecord object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelHistoryMessageRecordWithDefaults

`func NewOpenChannelHistoryMessageRecordWithDefaults() *OpenChannelHistoryMessageRecord`

NewOpenChannelHistoryMessageRecordWithDefaults instantiates a new OpenChannelHistoryMessageRecord object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelHistoryMessageRecord) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelHistoryMessageRecord) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelHistoryMessageRecord) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *OpenChannelHistoryMessageRecord) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetFromUserId

`func (o *OpenChannelHistoryMessageRecord) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *OpenChannelHistoryMessageRecord) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *OpenChannelHistoryMessageRecord) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.

### HasFromUserId

`func (o *OpenChannelHistoryMessageRecord) HasFromUserId() bool`

HasFromUserId returns a boolean if a field has been set.

### GetMessageId

`func (o *OpenChannelHistoryMessageRecord) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *OpenChannelHistoryMessageRecord) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *OpenChannelHistoryMessageRecord) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.

### HasMessageId

`func (o *OpenChannelHistoryMessageRecord) HasMessageId() bool`

HasMessageId returns a boolean if a field has been set.

### GetSentAt

`func (o *OpenChannelHistoryMessageRecord) GetSentAt() int64`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *OpenChannelHistoryMessageRecord) GetSentAtOk() (*int64, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *OpenChannelHistoryMessageRecord) SetSentAt(v int64)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *OpenChannelHistoryMessageRecord) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.

### GetMessageType

`func (o *OpenChannelHistoryMessageRecord) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *OpenChannelHistoryMessageRecord) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *OpenChannelHistoryMessageRecord) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.

### HasMessageType

`func (o *OpenChannelHistoryMessageRecord) HasMessageType() bool`

HasMessageType returns a boolean if a field has been set.

### GetContent

`func (o *OpenChannelHistoryMessageRecord) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *OpenChannelHistoryMessageRecord) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *OpenChannelHistoryMessageRecord) SetContent(v string)`

SetContent sets Content field to given value.

### HasContent

`func (o *OpenChannelHistoryMessageRecord) HasContent() bool`

HasContent returns a boolean if a field has been set.

### GetQuote

`func (o *OpenChannelHistoryMessageRecord) GetQuote() string`

GetQuote returns the Quote field if non-nil, zero value otherwise.

### GetQuoteOk

`func (o *OpenChannelHistoryMessageRecord) GetQuoteOk() (*string, bool)`

GetQuoteOk returns a tuple with the Quote field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQuote

`func (o *OpenChannelHistoryMessageRecord) SetQuote(v string)`

SetQuote sets Quote field to given value.

### HasQuote

`func (o *OpenChannelHistoryMessageRecord) HasQuote() bool`

HasQuote returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



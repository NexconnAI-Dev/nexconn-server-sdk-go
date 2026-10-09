# MessageRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Channel identifier of the stored message. | [optional] 
**SubchannelId** | Pointer to **string** | Community subchannel ID associated with the stored message, when applicable. | [optional] 
**FromUserId** | Pointer to **string** | Sender user ID of the stored message. | [optional] 
**MessageId** | Pointer to **string** | Unique message ID. | [optional] 
**SentAt** | Pointer to **int64** | Message send timestamp in milliseconds. | [optional] 
**MessageType** | Pointer to **string** | Message type of the stored message. | [optional] 
**Content** | Pointer to **string** | Raw message content payload as stored by the service. | [optional] 
**HasMetadata** | Pointer to **bool** | Whether the message has metadata entries attached. | [optional] 
**Metadata** | Pointer to [**[]MessageMetadataListItem**](MessageMetadataListItem.md) | Structured message metadata entries. Omitted when the original metadata is empty or cannot be parsed. | [optional] 
**Quote** | Pointer to **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional] 

## Methods

### NewMessageRecord

`func NewMessageRecord() *MessageRecord`

NewMessageRecord instantiates a new MessageRecord object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMessageRecordWithDefaults

`func NewMessageRecordWithDefaults() *MessageRecord`

NewMessageRecordWithDefaults instantiates a new MessageRecord object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *MessageRecord) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *MessageRecord) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *MessageRecord) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *MessageRecord) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetSubchannelId

`func (o *MessageRecord) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *MessageRecord) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *MessageRecord) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *MessageRecord) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetFromUserId

`func (o *MessageRecord) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *MessageRecord) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *MessageRecord) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.

### HasFromUserId

`func (o *MessageRecord) HasFromUserId() bool`

HasFromUserId returns a boolean if a field has been set.

### GetMessageId

`func (o *MessageRecord) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *MessageRecord) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *MessageRecord) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.

### HasMessageId

`func (o *MessageRecord) HasMessageId() bool`

HasMessageId returns a boolean if a field has been set.

### GetSentAt

`func (o *MessageRecord) GetSentAt() int64`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *MessageRecord) GetSentAtOk() (*int64, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *MessageRecord) SetSentAt(v int64)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *MessageRecord) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.

### GetMessageType

`func (o *MessageRecord) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *MessageRecord) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *MessageRecord) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.

### HasMessageType

`func (o *MessageRecord) HasMessageType() bool`

HasMessageType returns a boolean if a field has been set.

### GetContent

`func (o *MessageRecord) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *MessageRecord) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *MessageRecord) SetContent(v string)`

SetContent sets Content field to given value.

### HasContent

`func (o *MessageRecord) HasContent() bool`

HasContent returns a boolean if a field has been set.

### GetHasMetadata

`func (o *MessageRecord) GetHasMetadata() bool`

GetHasMetadata returns the HasMetadata field if non-nil, zero value otherwise.

### GetHasMetadataOk

`func (o *MessageRecord) GetHasMetadataOk() (*bool, bool)`

GetHasMetadataOk returns a tuple with the HasMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMetadata

`func (o *MessageRecord) SetHasMetadata(v bool)`

SetHasMetadata sets HasMetadata field to given value.

### HasHasMetadata

`func (o *MessageRecord) HasHasMetadata() bool`

HasHasMetadata returns a boolean if a field has been set.

### GetMetadata

`func (o *MessageRecord) GetMetadata() []MessageMetadataListItem`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *MessageRecord) GetMetadataOk() (*[]MessageMetadataListItem, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *MessageRecord) SetMetadata(v []MessageMetadataListItem)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *MessageRecord) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetQuote

`func (o *MessageRecord) GetQuote() string`

GetQuote returns the Quote field if non-nil, zero value otherwise.

### GetQuoteOk

`func (o *MessageRecord) GetQuoteOk() (*string, bool)`

GetQuoteOk returns a tuple with the Quote field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQuote

`func (o *MessageRecord) SetQuote(v string)`

SetQuote sets Quote field to given value.

### HasQuote

`func (o *MessageRecord) HasQuote() bool`

HasQuote returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# DirectGroupHistoryMessageRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** | Channel identifier of the stored message. | [optional] 
**FromUserId** | Pointer to **string** | Sender user ID of the stored message. | [optional] 
**MessageId** | Pointer to **string** | Unique message ID. | [optional] 
**SentAt** | Pointer to **int64** | Message send timestamp in milliseconds. | [optional] 
**MessageType** | Pointer to **string** | Message type of the stored message. | [optional] 
**Content** | Pointer to **string** | Raw message content payload as stored by the service. | [optional] 
**HasMetadata** | Pointer to **bool** | Whether the message has metadata entries attached. | [optional] 
**Metadata** | Pointer to [**[]MessageMetadataListItem**](MessageMetadataListItem.md) | Structured message metadata entries. Omitted when the original metadata is empty or cannot be parsed. | [optional] 
**AiGenerated** | Pointer to **bool** | Whether the message was AI-generated. Returned only for direct and group channels when the application has enabled this capability. | [optional] 
**Quote** | Pointer to **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional] 

## Methods

### NewDirectGroupHistoryMessageRecord

`func NewDirectGroupHistoryMessageRecord() *DirectGroupHistoryMessageRecord`

NewDirectGroupHistoryMessageRecord instantiates a new DirectGroupHistoryMessageRecord object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDirectGroupHistoryMessageRecordWithDefaults

`func NewDirectGroupHistoryMessageRecordWithDefaults() *DirectGroupHistoryMessageRecord`

NewDirectGroupHistoryMessageRecordWithDefaults instantiates a new DirectGroupHistoryMessageRecord object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *DirectGroupHistoryMessageRecord) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *DirectGroupHistoryMessageRecord) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *DirectGroupHistoryMessageRecord) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *DirectGroupHistoryMessageRecord) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetFromUserId

`func (o *DirectGroupHistoryMessageRecord) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *DirectGroupHistoryMessageRecord) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *DirectGroupHistoryMessageRecord) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.

### HasFromUserId

`func (o *DirectGroupHistoryMessageRecord) HasFromUserId() bool`

HasFromUserId returns a boolean if a field has been set.

### GetMessageId

`func (o *DirectGroupHistoryMessageRecord) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *DirectGroupHistoryMessageRecord) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *DirectGroupHistoryMessageRecord) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.

### HasMessageId

`func (o *DirectGroupHistoryMessageRecord) HasMessageId() bool`

HasMessageId returns a boolean if a field has been set.

### GetSentAt

`func (o *DirectGroupHistoryMessageRecord) GetSentAt() int64`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *DirectGroupHistoryMessageRecord) GetSentAtOk() (*int64, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *DirectGroupHistoryMessageRecord) SetSentAt(v int64)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *DirectGroupHistoryMessageRecord) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.

### GetMessageType

`func (o *DirectGroupHistoryMessageRecord) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *DirectGroupHistoryMessageRecord) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *DirectGroupHistoryMessageRecord) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.

### HasMessageType

`func (o *DirectGroupHistoryMessageRecord) HasMessageType() bool`

HasMessageType returns a boolean if a field has been set.

### GetContent

`func (o *DirectGroupHistoryMessageRecord) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *DirectGroupHistoryMessageRecord) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *DirectGroupHistoryMessageRecord) SetContent(v string)`

SetContent sets Content field to given value.

### HasContent

`func (o *DirectGroupHistoryMessageRecord) HasContent() bool`

HasContent returns a boolean if a field has been set.

### GetHasMetadata

`func (o *DirectGroupHistoryMessageRecord) GetHasMetadata() bool`

GetHasMetadata returns the HasMetadata field if non-nil, zero value otherwise.

### GetHasMetadataOk

`func (o *DirectGroupHistoryMessageRecord) GetHasMetadataOk() (*bool, bool)`

GetHasMetadataOk returns a tuple with the HasMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMetadata

`func (o *DirectGroupHistoryMessageRecord) SetHasMetadata(v bool)`

SetHasMetadata sets HasMetadata field to given value.

### HasHasMetadata

`func (o *DirectGroupHistoryMessageRecord) HasHasMetadata() bool`

HasHasMetadata returns a boolean if a field has been set.

### GetMetadata

`func (o *DirectGroupHistoryMessageRecord) GetMetadata() []MessageMetadataListItem`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *DirectGroupHistoryMessageRecord) GetMetadataOk() (*[]MessageMetadataListItem, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *DirectGroupHistoryMessageRecord) SetMetadata(v []MessageMetadataListItem)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *DirectGroupHistoryMessageRecord) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.

### GetAiGenerated

`func (o *DirectGroupHistoryMessageRecord) GetAiGenerated() bool`

GetAiGenerated returns the AiGenerated field if non-nil, zero value otherwise.

### GetAiGeneratedOk

`func (o *DirectGroupHistoryMessageRecord) GetAiGeneratedOk() (*bool, bool)`

GetAiGeneratedOk returns a tuple with the AiGenerated field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAiGenerated

`func (o *DirectGroupHistoryMessageRecord) SetAiGenerated(v bool)`

SetAiGenerated sets AiGenerated field to given value.

### HasAiGenerated

`func (o *DirectGroupHistoryMessageRecord) HasAiGenerated() bool`

HasAiGenerated returns a boolean if a field has been set.

### GetQuote

`func (o *DirectGroupHistoryMessageRecord) GetQuote() string`

GetQuote returns the Quote field if non-nil, zero value otherwise.

### GetQuoteOk

`func (o *DirectGroupHistoryMessageRecord) GetQuoteOk() (*string, bool)`

GetQuoteOk returns a tuple with the Quote field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQuote

`func (o *DirectGroupHistoryMessageRecord) SetQuote(v string)`

SetQuote sets Quote field to given value.

### HasQuote

`func (o *DirectGroupHistoryMessageRecord) HasQuote() bool`

HasQuote returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



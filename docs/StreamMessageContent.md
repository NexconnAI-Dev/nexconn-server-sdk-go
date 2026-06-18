# StreamMessageContent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **string** | Stream data chunk. Total message size must not exceed 128 KB across all chunks. | 
**Seq** | **int64** | Sequence number. Must be greater than 0, starting from 1, strictly incrementing and continuous. | 
**Complete** | **bool** | Whether this is the final chunk in the stream. &#x60;true&#x60; marks the end of the stream. | 
**CompleteReason** | Pointer to **int32** | Custom completion reason code. Only effective when &#x60;complete&#x60; is &#x60;true&#x60;. | [optional] 
**Type** | Pointer to **string** | Stream content type. Supported on the first chunk only. Default: text. Supported values: text, markdown, html. | [optional] 
**MessageId** | Pointer to **string** | Stream message unique ID. Not required for the first chunk. Required for subsequent chunks (use the value returned in the first chunk response). | [optional] 
**User** | Pointer to **map[string]interface{}** | Sender user information object. Supported on the first chunk only. | [optional] 
**MentionedInfo** | Pointer to **map[string]interface{}** | @mention information. Supported on the first chunk only. | [optional] 
**Extra** | Pointer to **map[string]interface{}** | Extension information. Supported on the first chunk only. | [optional] 

## Methods

### NewStreamMessageContent

`func NewStreamMessageContent(content string, seq int64, complete bool, ) *StreamMessageContent`

NewStreamMessageContent instantiates a new StreamMessageContent object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewStreamMessageContentWithDefaults

`func NewStreamMessageContentWithDefaults() *StreamMessageContent`

NewStreamMessageContentWithDefaults instantiates a new StreamMessageContent object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetContent

`func (o *StreamMessageContent) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *StreamMessageContent) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *StreamMessageContent) SetContent(v string)`

SetContent sets Content field to given value.


### GetSeq

`func (o *StreamMessageContent) GetSeq() int64`

GetSeq returns the Seq field if non-nil, zero value otherwise.

### GetSeqOk

`func (o *StreamMessageContent) GetSeqOk() (*int64, bool)`

GetSeqOk returns a tuple with the Seq field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeq

`func (o *StreamMessageContent) SetSeq(v int64)`

SetSeq sets Seq field to given value.


### GetComplete

`func (o *StreamMessageContent) GetComplete() bool`

GetComplete returns the Complete field if non-nil, zero value otherwise.

### GetCompleteOk

`func (o *StreamMessageContent) GetCompleteOk() (*bool, bool)`

GetCompleteOk returns a tuple with the Complete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetComplete

`func (o *StreamMessageContent) SetComplete(v bool)`

SetComplete sets Complete field to given value.


### GetCompleteReason

`func (o *StreamMessageContent) GetCompleteReason() int32`

GetCompleteReason returns the CompleteReason field if non-nil, zero value otherwise.

### GetCompleteReasonOk

`func (o *StreamMessageContent) GetCompleteReasonOk() (*int32, bool)`

GetCompleteReasonOk returns a tuple with the CompleteReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCompleteReason

`func (o *StreamMessageContent) SetCompleteReason(v int32)`

SetCompleteReason sets CompleteReason field to given value.

### HasCompleteReason

`func (o *StreamMessageContent) HasCompleteReason() bool`

HasCompleteReason returns a boolean if a field has been set.

### GetType

`func (o *StreamMessageContent) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *StreamMessageContent) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *StreamMessageContent) SetType(v string)`

SetType sets Type field to given value.

### HasType

`func (o *StreamMessageContent) HasType() bool`

HasType returns a boolean if a field has been set.

### GetMessageId

`func (o *StreamMessageContent) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *StreamMessageContent) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *StreamMessageContent) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.

### HasMessageId

`func (o *StreamMessageContent) HasMessageId() bool`

HasMessageId returns a boolean if a field has been set.

### GetUser

`func (o *StreamMessageContent) GetUser() map[string]interface{}`

GetUser returns the User field if non-nil, zero value otherwise.

### GetUserOk

`func (o *StreamMessageContent) GetUserOk() (*map[string]interface{}, bool)`

GetUserOk returns a tuple with the User field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUser

`func (o *StreamMessageContent) SetUser(v map[string]interface{})`

SetUser sets User field to given value.

### HasUser

`func (o *StreamMessageContent) HasUser() bool`

HasUser returns a boolean if a field has been set.

### GetMentionedInfo

`func (o *StreamMessageContent) GetMentionedInfo() map[string]interface{}`

GetMentionedInfo returns the MentionedInfo field if non-nil, zero value otherwise.

### GetMentionedInfoOk

`func (o *StreamMessageContent) GetMentionedInfoOk() (*map[string]interface{}, bool)`

GetMentionedInfoOk returns a tuple with the MentionedInfo field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMentionedInfo

`func (o *StreamMessageContent) SetMentionedInfo(v map[string]interface{})`

SetMentionedInfo sets MentionedInfo field to given value.

### HasMentionedInfo

`func (o *StreamMessageContent) HasMentionedInfo() bool`

HasMentionedInfo returns a boolean if a field has been set.

### GetExtra

`func (o *StreamMessageContent) GetExtra() map[string]interface{}`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *StreamMessageContent) GetExtraOk() (*map[string]interface{}, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *StreamMessageContent) SetExtra(v map[string]interface{})`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *StreamMessageContent) HasExtra() bool`

HasExtra returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



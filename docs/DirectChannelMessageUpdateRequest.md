# DirectChannelMessageUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** |  | 
**TargetId** | **string** | Direct-channel target user ID. | 
**MessageId** | **string** |  | 
**Content** | **string** |  | 

## Methods

### NewDirectChannelMessageUpdateRequest

`func NewDirectChannelMessageUpdateRequest(fromUserId string, targetId string, messageId string, content string, ) *DirectChannelMessageUpdateRequest`

NewDirectChannelMessageUpdateRequest instantiates a new DirectChannelMessageUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDirectChannelMessageUpdateRequestWithDefaults

`func NewDirectChannelMessageUpdateRequestWithDefaults() *DirectChannelMessageUpdateRequest`

NewDirectChannelMessageUpdateRequestWithDefaults instantiates a new DirectChannelMessageUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *DirectChannelMessageUpdateRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *DirectChannelMessageUpdateRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *DirectChannelMessageUpdateRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetTargetId

`func (o *DirectChannelMessageUpdateRequest) GetTargetId() string`

GetTargetId returns the TargetId field if non-nil, zero value otherwise.

### GetTargetIdOk

`func (o *DirectChannelMessageUpdateRequest) GetTargetIdOk() (*string, bool)`

GetTargetIdOk returns a tuple with the TargetId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetId

`func (o *DirectChannelMessageUpdateRequest) SetTargetId(v string)`

SetTargetId sets TargetId field to given value.


### GetMessageId

`func (o *DirectChannelMessageUpdateRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *DirectChannelMessageUpdateRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *DirectChannelMessageUpdateRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetContent

`func (o *DirectChannelMessageUpdateRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *DirectChannelMessageUpdateRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *DirectChannelMessageUpdateRequest) SetContent(v string)`

SetContent sets Content field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



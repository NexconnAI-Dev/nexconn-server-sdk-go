# SystemChannelPushMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **string** |  | 
**MessageType** | **string** |  | 
**DisableUpdateLastMsg** | Pointer to **bool** |  | [optional] 

## Methods

### NewSystemChannelPushMessage

`func NewSystemChannelPushMessage(content string, messageType string, ) *SystemChannelPushMessage`

NewSystemChannelPushMessage instantiates a new SystemChannelPushMessage object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelPushMessageWithDefaults

`func NewSystemChannelPushMessageWithDefaults() *SystemChannelPushMessage`

NewSystemChannelPushMessageWithDefaults instantiates a new SystemChannelPushMessage object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetContent

`func (o *SystemChannelPushMessage) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *SystemChannelPushMessage) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *SystemChannelPushMessage) SetContent(v string)`

SetContent sets Content field to given value.


### GetMessageType

`func (o *SystemChannelPushMessage) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *SystemChannelPushMessage) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *SystemChannelPushMessage) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetDisableUpdateLastMsg

`func (o *SystemChannelPushMessage) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *SystemChannelPushMessage) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *SystemChannelPushMessage) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *SystemChannelPushMessage) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



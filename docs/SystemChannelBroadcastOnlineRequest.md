# SystemChannelBroadcastOnlineRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** |  | 
**MessageType** | **string** |  | 
**Content** | **string** |  | 
**DisableUpdateLastMsg** | Pointer to **bool** |  | [optional] 

## Methods

### NewSystemChannelBroadcastOnlineRequest

`func NewSystemChannelBroadcastOnlineRequest(fromUserId string, messageType string, content string, ) *SystemChannelBroadcastOnlineRequest`

NewSystemChannelBroadcastOnlineRequest instantiates a new SystemChannelBroadcastOnlineRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelBroadcastOnlineRequestWithDefaults

`func NewSystemChannelBroadcastOnlineRequestWithDefaults() *SystemChannelBroadcastOnlineRequest`

NewSystemChannelBroadcastOnlineRequestWithDefaults instantiates a new SystemChannelBroadcastOnlineRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *SystemChannelBroadcastOnlineRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *SystemChannelBroadcastOnlineRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *SystemChannelBroadcastOnlineRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetMessageType

`func (o *SystemChannelBroadcastOnlineRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *SystemChannelBroadcastOnlineRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *SystemChannelBroadcastOnlineRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *SystemChannelBroadcastOnlineRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *SystemChannelBroadcastOnlineRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *SystemChannelBroadcastOnlineRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastOnlineRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *SystemChannelBroadcastOnlineRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastOnlineRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *SystemChannelBroadcastOnlineRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



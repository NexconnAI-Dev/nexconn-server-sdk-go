# SystemChannelBroadcastAllRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** |  | 
**MessageType** | **string** |  | 
**Content** | **string** |  | 
**PushContent** | Pointer to **string** |  | [optional] 
**PushData** | Pointer to **string** |  | [optional] 
**ContentAvailable** | Pointer to **int32** |  | [optional] 
**PushExt** | Pointer to **string** | Extended push configuration (JSON string as accepted by &#x60;MessageBroadcastInput&#x60;). | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** |  | [optional] 

## Methods

### NewSystemChannelBroadcastAllRequest

`func NewSystemChannelBroadcastAllRequest(fromUserId string, messageType string, content string, ) *SystemChannelBroadcastAllRequest`

NewSystemChannelBroadcastAllRequest instantiates a new SystemChannelBroadcastAllRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelBroadcastAllRequestWithDefaults

`func NewSystemChannelBroadcastAllRequestWithDefaults() *SystemChannelBroadcastAllRequest`

NewSystemChannelBroadcastAllRequestWithDefaults instantiates a new SystemChannelBroadcastAllRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *SystemChannelBroadcastAllRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *SystemChannelBroadcastAllRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *SystemChannelBroadcastAllRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetMessageType

`func (o *SystemChannelBroadcastAllRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *SystemChannelBroadcastAllRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *SystemChannelBroadcastAllRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *SystemChannelBroadcastAllRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *SystemChannelBroadcastAllRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *SystemChannelBroadcastAllRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetPushContent

`func (o *SystemChannelBroadcastAllRequest) GetPushContent() string`

GetPushContent returns the PushContent field if non-nil, zero value otherwise.

### GetPushContentOk

`func (o *SystemChannelBroadcastAllRequest) GetPushContentOk() (*string, bool)`

GetPushContentOk returns a tuple with the PushContent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushContent

`func (o *SystemChannelBroadcastAllRequest) SetPushContent(v string)`

SetPushContent sets PushContent field to given value.

### HasPushContent

`func (o *SystemChannelBroadcastAllRequest) HasPushContent() bool`

HasPushContent returns a boolean if a field has been set.

### GetPushData

`func (o *SystemChannelBroadcastAllRequest) GetPushData() string`

GetPushData returns the PushData field if non-nil, zero value otherwise.

### GetPushDataOk

`func (o *SystemChannelBroadcastAllRequest) GetPushDataOk() (*string, bool)`

GetPushDataOk returns a tuple with the PushData field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushData

`func (o *SystemChannelBroadcastAllRequest) SetPushData(v string)`

SetPushData sets PushData field to given value.

### HasPushData

`func (o *SystemChannelBroadcastAllRequest) HasPushData() bool`

HasPushData returns a boolean if a field has been set.

### GetContentAvailable

`func (o *SystemChannelBroadcastAllRequest) GetContentAvailable() int32`

GetContentAvailable returns the ContentAvailable field if non-nil, zero value otherwise.

### GetContentAvailableOk

`func (o *SystemChannelBroadcastAllRequest) GetContentAvailableOk() (*int32, bool)`

GetContentAvailableOk returns a tuple with the ContentAvailable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContentAvailable

`func (o *SystemChannelBroadcastAllRequest) SetContentAvailable(v int32)`

SetContentAvailable sets ContentAvailable field to given value.

### HasContentAvailable

`func (o *SystemChannelBroadcastAllRequest) HasContentAvailable() bool`

HasContentAvailable returns a boolean if a field has been set.

### GetPushExt

`func (o *SystemChannelBroadcastAllRequest) GetPushExt() string`

GetPushExt returns the PushExt field if non-nil, zero value otherwise.

### GetPushExtOk

`func (o *SystemChannelBroadcastAllRequest) GetPushExtOk() (*string, bool)`

GetPushExtOk returns a tuple with the PushExt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushExt

`func (o *SystemChannelBroadcastAllRequest) SetPushExt(v string)`

SetPushExt sets PushExt field to given value.

### HasPushExt

`func (o *SystemChannelBroadcastAllRequest) HasPushExt() bool`

HasPushExt returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastAllRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *SystemChannelBroadcastAllRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastAllRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *SystemChannelBroadcastAllRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



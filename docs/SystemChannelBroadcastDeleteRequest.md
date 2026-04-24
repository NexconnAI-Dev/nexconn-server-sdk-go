# SystemChannelBroadcastDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** |  | 
**MessageId** | **string** |  | 
**SentAt** | Pointer to **int64** |  | [optional] 
**IsAdmin** | Pointer to **int32** |  | [optional] 
**Extra** | Pointer to **string** |  | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** |  | [optional] 

## Methods

### NewSystemChannelBroadcastDeleteRequest

`func NewSystemChannelBroadcastDeleteRequest(fromUserId string, messageId string, ) *SystemChannelBroadcastDeleteRequest`

NewSystemChannelBroadcastDeleteRequest instantiates a new SystemChannelBroadcastDeleteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelBroadcastDeleteRequestWithDefaults

`func NewSystemChannelBroadcastDeleteRequestWithDefaults() *SystemChannelBroadcastDeleteRequest`

NewSystemChannelBroadcastDeleteRequestWithDefaults instantiates a new SystemChannelBroadcastDeleteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *SystemChannelBroadcastDeleteRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *SystemChannelBroadcastDeleteRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *SystemChannelBroadcastDeleteRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetMessageId

`func (o *SystemChannelBroadcastDeleteRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *SystemChannelBroadcastDeleteRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *SystemChannelBroadcastDeleteRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetSentAt

`func (o *SystemChannelBroadcastDeleteRequest) GetSentAt() int64`

GetSentAt returns the SentAt field if non-nil, zero value otherwise.

### GetSentAtOk

`func (o *SystemChannelBroadcastDeleteRequest) GetSentAtOk() (*int64, bool)`

GetSentAtOk returns a tuple with the SentAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSentAt

`func (o *SystemChannelBroadcastDeleteRequest) SetSentAt(v int64)`

SetSentAt sets SentAt field to given value.

### HasSentAt

`func (o *SystemChannelBroadcastDeleteRequest) HasSentAt() bool`

HasSentAt returns a boolean if a field has been set.

### GetIsAdmin

`func (o *SystemChannelBroadcastDeleteRequest) GetIsAdmin() int32`

GetIsAdmin returns the IsAdmin field if non-nil, zero value otherwise.

### GetIsAdminOk

`func (o *SystemChannelBroadcastDeleteRequest) GetIsAdminOk() (*int32, bool)`

GetIsAdminOk returns a tuple with the IsAdmin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsAdmin

`func (o *SystemChannelBroadcastDeleteRequest) SetIsAdmin(v int32)`

SetIsAdmin sets IsAdmin field to given value.

### HasIsAdmin

`func (o *SystemChannelBroadcastDeleteRequest) HasIsAdmin() bool`

HasIsAdmin returns a boolean if a field has been set.

### GetExtra

`func (o *SystemChannelBroadcastDeleteRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *SystemChannelBroadcastDeleteRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *SystemChannelBroadcastDeleteRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *SystemChannelBroadcastDeleteRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastDeleteRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *SystemChannelBroadcastDeleteRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *SystemChannelBroadcastDeleteRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *SystemChannelBroadcastDeleteRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# SystemChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. The sender should have an access token. | 
**ToUserIds** | **[]string** | Recipient user IDs. Up to 100 users are supported in a single request. | 
**MessageType** | **string** | Message type. Supports built-in types and custom types. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | 
**PushContent** | Pointer to **string** | Push notification text for offline recipients. Required for custom or notification messages that need push delivery. | [optional] 
**PushData** | Pointer to **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on iOS and Android. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**ContentAvailable** | Pointer to **int32** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] 
**DisablePush** | Pointer to **bool** | Whether to suppress push notifications for offline recipients. | [optional] 
**PushExt** | Pointer to **string** | Extended push configuration (JSON string as accepted by &#x60;SystemChannelMsgSendInput&#x60;). | [optional] 
**DisableUpdateLastMsg** | Pointer to **bool** | Whether to keep this message from updating the system channel&#39;s last-message preview. | [optional] 

## Methods

### NewSystemChannelMessageSendRequest

`func NewSystemChannelMessageSendRequest(fromUserId string, toUserIds []string, messageType string, content string, ) *SystemChannelMessageSendRequest`

NewSystemChannelMessageSendRequest instantiates a new SystemChannelMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelMessageSendRequestWithDefaults

`func NewSystemChannelMessageSendRequestWithDefaults() *SystemChannelMessageSendRequest`

NewSystemChannelMessageSendRequestWithDefaults instantiates a new SystemChannelMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *SystemChannelMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *SystemChannelMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *SystemChannelMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToUserIds

`func (o *SystemChannelMessageSendRequest) GetToUserIds() []string`

GetToUserIds returns the ToUserIds field if non-nil, zero value otherwise.

### GetToUserIdsOk

`func (o *SystemChannelMessageSendRequest) GetToUserIdsOk() (*[]string, bool)`

GetToUserIdsOk returns a tuple with the ToUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserIds

`func (o *SystemChannelMessageSendRequest) SetToUserIds(v []string)`

SetToUserIds sets ToUserIds field to given value.


### GetMessageType

`func (o *SystemChannelMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *SystemChannelMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *SystemChannelMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *SystemChannelMessageSendRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *SystemChannelMessageSendRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *SystemChannelMessageSendRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetPushContent

`func (o *SystemChannelMessageSendRequest) GetPushContent() string`

GetPushContent returns the PushContent field if non-nil, zero value otherwise.

### GetPushContentOk

`func (o *SystemChannelMessageSendRequest) GetPushContentOk() (*string, bool)`

GetPushContentOk returns a tuple with the PushContent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushContent

`func (o *SystemChannelMessageSendRequest) SetPushContent(v string)`

SetPushContent sets PushContent field to given value.

### HasPushContent

`func (o *SystemChannelMessageSendRequest) HasPushContent() bool`

HasPushContent returns a boolean if a field has been set.

### GetPushData

`func (o *SystemChannelMessageSendRequest) GetPushData() string`

GetPushData returns the PushData field if non-nil, zero value otherwise.

### GetPushDataOk

`func (o *SystemChannelMessageSendRequest) GetPushDataOk() (*string, bool)`

GetPushDataOk returns a tuple with the PushData field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushData

`func (o *SystemChannelMessageSendRequest) SetPushData(v string)`

SetPushData sets PushData field to given value.

### HasPushData

`func (o *SystemChannelMessageSendRequest) HasPushData() bool`

HasPushData returns a boolean if a field has been set.

### GetShouldPersist

`func (o *SystemChannelMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *SystemChannelMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *SystemChannelMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *SystemChannelMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetContentAvailable

`func (o *SystemChannelMessageSendRequest) GetContentAvailable() int32`

GetContentAvailable returns the ContentAvailable field if non-nil, zero value otherwise.

### GetContentAvailableOk

`func (o *SystemChannelMessageSendRequest) GetContentAvailableOk() (*int32, bool)`

GetContentAvailableOk returns a tuple with the ContentAvailable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContentAvailable

`func (o *SystemChannelMessageSendRequest) SetContentAvailable(v int32)`

SetContentAvailable sets ContentAvailable field to given value.

### HasContentAvailable

`func (o *SystemChannelMessageSendRequest) HasContentAvailable() bool`

HasContentAvailable returns a boolean if a field has been set.

### GetDisablePush

`func (o *SystemChannelMessageSendRequest) GetDisablePush() bool`

GetDisablePush returns the DisablePush field if non-nil, zero value otherwise.

### GetDisablePushOk

`func (o *SystemChannelMessageSendRequest) GetDisablePushOk() (*bool, bool)`

GetDisablePushOk returns a tuple with the DisablePush field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisablePush

`func (o *SystemChannelMessageSendRequest) SetDisablePush(v bool)`

SetDisablePush sets DisablePush field to given value.

### HasDisablePush

`func (o *SystemChannelMessageSendRequest) HasDisablePush() bool`

HasDisablePush returns a boolean if a field has been set.

### GetPushExt

`func (o *SystemChannelMessageSendRequest) GetPushExt() string`

GetPushExt returns the PushExt field if non-nil, zero value otherwise.

### GetPushExtOk

`func (o *SystemChannelMessageSendRequest) GetPushExtOk() (*string, bool)`

GetPushExtOk returns a tuple with the PushExt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushExt

`func (o *SystemChannelMessageSendRequest) SetPushExt(v string)`

SetPushExt sets PushExt field to given value.

### HasPushExt

`func (o *SystemChannelMessageSendRequest) HasPushExt() bool`

HasPushExt returns a boolean if a field has been set.

### GetDisableUpdateLastMsg

`func (o *SystemChannelMessageSendRequest) GetDisableUpdateLastMsg() bool`

GetDisableUpdateLastMsg returns the DisableUpdateLastMsg field if non-nil, zero value otherwise.

### GetDisableUpdateLastMsgOk

`func (o *SystemChannelMessageSendRequest) GetDisableUpdateLastMsgOk() (*bool, bool)`

GetDisableUpdateLastMsgOk returns a tuple with the DisableUpdateLastMsg field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisableUpdateLastMsg

`func (o *SystemChannelMessageSendRequest) SetDisableUpdateLastMsg(v bool)`

SetDisableUpdateLastMsg sets DisableUpdateLastMsg field to given value.

### HasDisableUpdateLastMsg

`func (o *SystemChannelMessageSendRequest) HasDisableUpdateLastMsg() bool`

HasDisableUpdateLastMsg returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



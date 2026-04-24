# CommunityChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromUserId** | **string** | Sender user ID. Non-members can send through the server API, but push display works best when the sender has an access token. | 
**ToChannelIds** | **[]string** | Target community channel IDs. Up to 3 community channels are supported per request. | 
**ToUserIds** | Pointer to **[]string** | Recipient member user IDs for a targeted community message. Only effective when sending to a single community channel. | [optional] 
**MessageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | 
**Content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | 
**PushContent** | Pointer to **string** | Push notification text for offline recipients. Optional for built-in user content messages and required for push-enabled custom or notification messages. | [optional] 
**PushData** | Pointer to **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on mobile push payloads. | [optional] 
**ShouldPersist** | Pointer to **int32** | Whether to store the message in community message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] 
**IsCounted** | Pointer to **int32** | Whether to count this message as unread for offline users. &#x60;1&#x60; counts as unread and &#x60;0&#x60; does not. | [optional] 
**HasMention** | Pointer to **int32** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional] 
**ContentAvailable** | Pointer to **int32** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] 
**PushExt** | Pointer to **string** | Extended push configuration (JSON string as accepted by the server &#x60;CommunityChannelMsgSendInput&#x60;). | [optional] 
**SubchannelId** | Pointer to **string** | Target subchannel ID. If omitted, delivery follows the app&#39;s default community-channel behavior. | [optional] 
**HasMetadata** | Pointer to **bool** | Whether to enable message metadata for this message. | [optional] 
**Metadata** | Pointer to **map[string]interface{}** | Custom message metadata entries. Only effective when &#x60;hasMetadata&#x60; is &#x60;true&#x60;. | [optional] 

## Methods

### NewCommunityChannelMessageSendRequest

`func NewCommunityChannelMessageSendRequest(fromUserId string, toChannelIds []string, messageType string, content string, ) *CommunityChannelMessageSendRequest`

NewCommunityChannelMessageSendRequest instantiates a new CommunityChannelMessageSendRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageSendRequestWithDefaults

`func NewCommunityChannelMessageSendRequestWithDefaults() *CommunityChannelMessageSendRequest`

NewCommunityChannelMessageSendRequestWithDefaults instantiates a new CommunityChannelMessageSendRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromUserId

`func (o *CommunityChannelMessageSendRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *CommunityChannelMessageSendRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *CommunityChannelMessageSendRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetToChannelIds

`func (o *CommunityChannelMessageSendRequest) GetToChannelIds() []string`

GetToChannelIds returns the ToChannelIds field if non-nil, zero value otherwise.

### GetToChannelIdsOk

`func (o *CommunityChannelMessageSendRequest) GetToChannelIdsOk() (*[]string, bool)`

GetToChannelIdsOk returns a tuple with the ToChannelIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToChannelIds

`func (o *CommunityChannelMessageSendRequest) SetToChannelIds(v []string)`

SetToChannelIds sets ToChannelIds field to given value.


### GetToUserIds

`func (o *CommunityChannelMessageSendRequest) GetToUserIds() []string`

GetToUserIds returns the ToUserIds field if non-nil, zero value otherwise.

### GetToUserIdsOk

`func (o *CommunityChannelMessageSendRequest) GetToUserIdsOk() (*[]string, bool)`

GetToUserIdsOk returns a tuple with the ToUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToUserIds

`func (o *CommunityChannelMessageSendRequest) SetToUserIds(v []string)`

SetToUserIds sets ToUserIds field to given value.

### HasToUserIds

`func (o *CommunityChannelMessageSendRequest) HasToUserIds() bool`

HasToUserIds returns a boolean if a field has been set.

### GetMessageType

`func (o *CommunityChannelMessageSendRequest) GetMessageType() string`

GetMessageType returns the MessageType field if non-nil, zero value otherwise.

### GetMessageTypeOk

`func (o *CommunityChannelMessageSendRequest) GetMessageTypeOk() (*string, bool)`

GetMessageTypeOk returns a tuple with the MessageType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageType

`func (o *CommunityChannelMessageSendRequest) SetMessageType(v string)`

SetMessageType sets MessageType field to given value.


### GetContent

`func (o *CommunityChannelMessageSendRequest) GetContent() string`

GetContent returns the Content field if non-nil, zero value otherwise.

### GetContentOk

`func (o *CommunityChannelMessageSendRequest) GetContentOk() (*string, bool)`

GetContentOk returns a tuple with the Content field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContent

`func (o *CommunityChannelMessageSendRequest) SetContent(v string)`

SetContent sets Content field to given value.


### GetPushContent

`func (o *CommunityChannelMessageSendRequest) GetPushContent() string`

GetPushContent returns the PushContent field if non-nil, zero value otherwise.

### GetPushContentOk

`func (o *CommunityChannelMessageSendRequest) GetPushContentOk() (*string, bool)`

GetPushContentOk returns a tuple with the PushContent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushContent

`func (o *CommunityChannelMessageSendRequest) SetPushContent(v string)`

SetPushContent sets PushContent field to given value.

### HasPushContent

`func (o *CommunityChannelMessageSendRequest) HasPushContent() bool`

HasPushContent returns a boolean if a field has been set.

### GetPushData

`func (o *CommunityChannelMessageSendRequest) GetPushData() string`

GetPushData returns the PushData field if non-nil, zero value otherwise.

### GetPushDataOk

`func (o *CommunityChannelMessageSendRequest) GetPushDataOk() (*string, bool)`

GetPushDataOk returns a tuple with the PushData field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushData

`func (o *CommunityChannelMessageSendRequest) SetPushData(v string)`

SetPushData sets PushData field to given value.

### HasPushData

`func (o *CommunityChannelMessageSendRequest) HasPushData() bool`

HasPushData returns a boolean if a field has been set.

### GetShouldPersist

`func (o *CommunityChannelMessageSendRequest) GetShouldPersist() int32`

GetShouldPersist returns the ShouldPersist field if non-nil, zero value otherwise.

### GetShouldPersistOk

`func (o *CommunityChannelMessageSendRequest) GetShouldPersistOk() (*int32, bool)`

GetShouldPersistOk returns a tuple with the ShouldPersist field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldPersist

`func (o *CommunityChannelMessageSendRequest) SetShouldPersist(v int32)`

SetShouldPersist sets ShouldPersist field to given value.

### HasShouldPersist

`func (o *CommunityChannelMessageSendRequest) HasShouldPersist() bool`

HasShouldPersist returns a boolean if a field has been set.

### GetIsCounted

`func (o *CommunityChannelMessageSendRequest) GetIsCounted() int32`

GetIsCounted returns the IsCounted field if non-nil, zero value otherwise.

### GetIsCountedOk

`func (o *CommunityChannelMessageSendRequest) GetIsCountedOk() (*int32, bool)`

GetIsCountedOk returns a tuple with the IsCounted field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsCounted

`func (o *CommunityChannelMessageSendRequest) SetIsCounted(v int32)`

SetIsCounted sets IsCounted field to given value.

### HasIsCounted

`func (o *CommunityChannelMessageSendRequest) HasIsCounted() bool`

HasIsCounted returns a boolean if a field has been set.

### GetHasMention

`func (o *CommunityChannelMessageSendRequest) GetHasMention() int32`

GetHasMention returns the HasMention field if non-nil, zero value otherwise.

### GetHasMentionOk

`func (o *CommunityChannelMessageSendRequest) GetHasMentionOk() (*int32, bool)`

GetHasMentionOk returns a tuple with the HasMention field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMention

`func (o *CommunityChannelMessageSendRequest) SetHasMention(v int32)`

SetHasMention sets HasMention field to given value.

### HasHasMention

`func (o *CommunityChannelMessageSendRequest) HasHasMention() bool`

HasHasMention returns a boolean if a field has been set.

### GetContentAvailable

`func (o *CommunityChannelMessageSendRequest) GetContentAvailable() int32`

GetContentAvailable returns the ContentAvailable field if non-nil, zero value otherwise.

### GetContentAvailableOk

`func (o *CommunityChannelMessageSendRequest) GetContentAvailableOk() (*int32, bool)`

GetContentAvailableOk returns a tuple with the ContentAvailable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContentAvailable

`func (o *CommunityChannelMessageSendRequest) SetContentAvailable(v int32)`

SetContentAvailable sets ContentAvailable field to given value.

### HasContentAvailable

`func (o *CommunityChannelMessageSendRequest) HasContentAvailable() bool`

HasContentAvailable returns a boolean if a field has been set.

### GetPushExt

`func (o *CommunityChannelMessageSendRequest) GetPushExt() string`

GetPushExt returns the PushExt field if non-nil, zero value otherwise.

### GetPushExtOk

`func (o *CommunityChannelMessageSendRequest) GetPushExtOk() (*string, bool)`

GetPushExtOk returns a tuple with the PushExt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushExt

`func (o *CommunityChannelMessageSendRequest) SetPushExt(v string)`

SetPushExt sets PushExt field to given value.

### HasPushExt

`func (o *CommunityChannelMessageSendRequest) HasPushExt() bool`

HasPushExt returns a boolean if a field has been set.

### GetSubchannelId

`func (o *CommunityChannelMessageSendRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelMessageSendRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelMessageSendRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelMessageSendRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetHasMetadata

`func (o *CommunityChannelMessageSendRequest) GetHasMetadata() bool`

GetHasMetadata returns the HasMetadata field if non-nil, zero value otherwise.

### GetHasMetadataOk

`func (o *CommunityChannelMessageSendRequest) GetHasMetadataOk() (*bool, bool)`

GetHasMetadataOk returns a tuple with the HasMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHasMetadata

`func (o *CommunityChannelMessageSendRequest) SetHasMetadata(v bool)`

SetHasMetadata sets HasMetadata field to given value.

### HasHasMetadata

`func (o *CommunityChannelMessageSendRequest) HasHasMetadata() bool`

HasHasMetadata returns a boolean if a field has been set.

### GetMetadata

`func (o *CommunityChannelMessageSendRequest) GetMetadata() map[string]interface{}`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *CommunityChannelMessageSendRequest) GetMetadataOk() (*map[string]interface{}, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *CommunityChannelMessageSendRequest) SetMetadata(v map[string]interface{})`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *CommunityChannelMessageSendRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



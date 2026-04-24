# OpenChannelMutedParticipantItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParticipantId** | Pointer to **string** |  | [optional] 
**MuteExpiresAt** | Pointer to **string** | Mute expiration time in &#x60;YYYY-MM-DD HH:MM:SS&#x60; format. | [optional] 

## Methods

### NewOpenChannelMutedParticipantItem

`func NewOpenChannelMutedParticipantItem() *OpenChannelMutedParticipantItem`

NewOpenChannelMutedParticipantItem instantiates a new OpenChannelMutedParticipantItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMutedParticipantItemWithDefaults

`func NewOpenChannelMutedParticipantItemWithDefaults() *OpenChannelMutedParticipantItem`

NewOpenChannelMutedParticipantItemWithDefaults instantiates a new OpenChannelMutedParticipantItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetParticipantId

`func (o *OpenChannelMutedParticipantItem) GetParticipantId() string`

GetParticipantId returns the ParticipantId field if non-nil, zero value otherwise.

### GetParticipantIdOk

`func (o *OpenChannelMutedParticipantItem) GetParticipantIdOk() (*string, bool)`

GetParticipantIdOk returns a tuple with the ParticipantId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantId

`func (o *OpenChannelMutedParticipantItem) SetParticipantId(v string)`

SetParticipantId sets ParticipantId field to given value.

### HasParticipantId

`func (o *OpenChannelMutedParticipantItem) HasParticipantId() bool`

HasParticipantId returns a boolean if a field has been set.

### GetMuteExpiresAt

`func (o *OpenChannelMutedParticipantItem) GetMuteExpiresAt() string`

GetMuteExpiresAt returns the MuteExpiresAt field if non-nil, zero value otherwise.

### GetMuteExpiresAtOk

`func (o *OpenChannelMutedParticipantItem) GetMuteExpiresAtOk() (*string, bool)`

GetMuteExpiresAtOk returns a tuple with the MuteExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMuteExpiresAt

`func (o *OpenChannelMutedParticipantItem) SetMuteExpiresAt(v string)`

SetMuteExpiresAt sets MuteExpiresAt field to given value.

### HasMuteExpiresAt

`func (o *OpenChannelMutedParticipantItem) HasMuteExpiresAt() bool`

HasMuteExpiresAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



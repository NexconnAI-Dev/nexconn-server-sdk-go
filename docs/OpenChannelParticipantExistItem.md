# OpenChannelParticipantExistItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParticipantId** | Pointer to **string** | User ID. | [optional] 
**IsInOpenChannel** | Pointer to **int32** | Whether the user is in the open channel. &#x60;1&#x60; &#x3D; yes, &#x60;0&#x60; &#x3D; no. | [optional] 

## Methods

### NewOpenChannelParticipantExistItem

`func NewOpenChannelParticipantExistItem() *OpenChannelParticipantExistItem`

NewOpenChannelParticipantExistItem instantiates a new OpenChannelParticipantExistItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantExistItemWithDefaults

`func NewOpenChannelParticipantExistItemWithDefaults() *OpenChannelParticipantExistItem`

NewOpenChannelParticipantExistItemWithDefaults instantiates a new OpenChannelParticipantExistItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetParticipantId

`func (o *OpenChannelParticipantExistItem) GetParticipantId() string`

GetParticipantId returns the ParticipantId field if non-nil, zero value otherwise.

### GetParticipantIdOk

`func (o *OpenChannelParticipantExistItem) GetParticipantIdOk() (*string, bool)`

GetParticipantIdOk returns a tuple with the ParticipantId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantId

`func (o *OpenChannelParticipantExistItem) SetParticipantId(v string)`

SetParticipantId sets ParticipantId field to given value.

### HasParticipantId

`func (o *OpenChannelParticipantExistItem) HasParticipantId() bool`

HasParticipantId returns a boolean if a field has been set.

### GetIsInOpenChannel

`func (o *OpenChannelParticipantExistItem) GetIsInOpenChannel() int32`

GetIsInOpenChannel returns the IsInOpenChannel field if non-nil, zero value otherwise.

### GetIsInOpenChannelOk

`func (o *OpenChannelParticipantExistItem) GetIsInOpenChannelOk() (*int32, bool)`

GetIsInOpenChannelOk returns a tuple with the IsInOpenChannel field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsInOpenChannel

`func (o *OpenChannelParticipantExistItem) SetIsInOpenChannel(v int32)`

SetIsInOpenChannel sets IsInOpenChannel field to given value.

### HasIsInOpenChannel

`func (o *OpenChannelParticipantExistItem) HasIsInOpenChannel() bool`

HasIsInOpenChannel returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



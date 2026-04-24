# OpenChannelParticipantExistResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Participants** | Pointer to [**[]OpenChannelParticipantExistItem**](OpenChannelParticipantExistItem.md) | Array of participant check results. | [optional] 

## Methods

### NewOpenChannelParticipantExistResponseResult

`func NewOpenChannelParticipantExistResponseResult() *OpenChannelParticipantExistResponseResult`

NewOpenChannelParticipantExistResponseResult instantiates a new OpenChannelParticipantExistResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantExistResponseResultWithDefaults

`func NewOpenChannelParticipantExistResponseResultWithDefaults() *OpenChannelParticipantExistResponseResult`

NewOpenChannelParticipantExistResponseResultWithDefaults instantiates a new OpenChannelParticipantExistResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetParticipants

`func (o *OpenChannelParticipantExistResponseResult) GetParticipants() []OpenChannelParticipantExistItem`

GetParticipants returns the Participants field if non-nil, zero value otherwise.

### GetParticipantsOk

`func (o *OpenChannelParticipantExistResponseResult) GetParticipantsOk() (*[]OpenChannelParticipantExistItem, bool)`

GetParticipantsOk returns a tuple with the Participants field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipants

`func (o *OpenChannelParticipantExistResponseResult) SetParticipants(v []OpenChannelParticipantExistItem)`

SetParticipants sets Participants field to given value.

### HasParticipants

`func (o *OpenChannelParticipantExistResponseResult) HasParticipants() bool`

HasParticipants returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



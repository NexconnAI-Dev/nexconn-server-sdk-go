# OpenChannelParticipantListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Total** | Pointer to **int32** |  | [optional] 
**Participants** | Pointer to [**[]OpenChannelParticipantItem**](OpenChannelParticipantItem.md) |  | [optional] 

## Methods

### NewOpenChannelParticipantListResponseResult

`func NewOpenChannelParticipantListResponseResult() *OpenChannelParticipantListResponseResult`

NewOpenChannelParticipantListResponseResult instantiates a new OpenChannelParticipantListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantListResponseResultWithDefaults

`func NewOpenChannelParticipantListResponseResultWithDefaults() *OpenChannelParticipantListResponseResult`

NewOpenChannelParticipantListResponseResultWithDefaults instantiates a new OpenChannelParticipantListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTotal

`func (o *OpenChannelParticipantListResponseResult) GetTotal() int32`

GetTotal returns the Total field if non-nil, zero value otherwise.

### GetTotalOk

`func (o *OpenChannelParticipantListResponseResult) GetTotalOk() (*int32, bool)`

GetTotalOk returns a tuple with the Total field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotal

`func (o *OpenChannelParticipantListResponseResult) SetTotal(v int32)`

SetTotal sets Total field to given value.

### HasTotal

`func (o *OpenChannelParticipantListResponseResult) HasTotal() bool`

HasTotal returns a boolean if a field has been set.

### GetParticipants

`func (o *OpenChannelParticipantListResponseResult) GetParticipants() []OpenChannelParticipantItem`

GetParticipants returns the Participants field if non-nil, zero value otherwise.

### GetParticipantsOk

`func (o *OpenChannelParticipantListResponseResult) GetParticipantsOk() (*[]OpenChannelParticipantItem, bool)`

GetParticipantsOk returns a tuple with the Participants field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipants

`func (o *OpenChannelParticipantListResponseResult) SetParticipants(v []OpenChannelParticipantItem)`

SetParticipants sets Participants field to given value.

### HasParticipants

`func (o *OpenChannelParticipantListResponseResult) HasParticipants() bool`

HasParticipants returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



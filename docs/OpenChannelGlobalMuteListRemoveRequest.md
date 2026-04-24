# OpenChannelGlobalMuteListRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParticipantIds** | **[]string** |  | 
**Extra** | Pointer to **string** | Notification extra payload in JSON string format. | [optional] 
**NeedNotify** | Pointer to **bool** |  | [optional] 

## Methods

### NewOpenChannelGlobalMuteListRemoveRequest

`func NewOpenChannelGlobalMuteListRemoveRequest(participantIds []string, ) *OpenChannelGlobalMuteListRemoveRequest`

NewOpenChannelGlobalMuteListRemoveRequest instantiates a new OpenChannelGlobalMuteListRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelGlobalMuteListRemoveRequestWithDefaults

`func NewOpenChannelGlobalMuteListRemoveRequestWithDefaults() *OpenChannelGlobalMuteListRemoveRequest`

NewOpenChannelGlobalMuteListRemoveRequestWithDefaults instantiates a new OpenChannelGlobalMuteListRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetParticipantIds

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetParticipantIds() []string`

GetParticipantIds returns the ParticipantIds field if non-nil, zero value otherwise.

### GetParticipantIdsOk

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetParticipantIdsOk() (*[]string, bool)`

GetParticipantIdsOk returns a tuple with the ParticipantIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantIds

`func (o *OpenChannelGlobalMuteListRemoveRequest) SetParticipantIds(v []string)`

SetParticipantIds sets ParticipantIds field to given value.


### GetExtra

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *OpenChannelGlobalMuteListRemoveRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *OpenChannelGlobalMuteListRemoveRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetNeedNotify

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetNeedNotify() bool`

GetNeedNotify returns the NeedNotify field if non-nil, zero value otherwise.

### GetNeedNotifyOk

`func (o *OpenChannelGlobalMuteListRemoveRequest) GetNeedNotifyOk() (*bool, bool)`

GetNeedNotifyOk returns a tuple with the NeedNotify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedNotify

`func (o *OpenChannelGlobalMuteListRemoveRequest) SetNeedNotify(v bool)`

SetNeedNotify sets NeedNotify field to given value.

### HasNeedNotify

`func (o *OpenChannelGlobalMuteListRemoveRequest) HasNeedNotify() bool`

HasNeedNotify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



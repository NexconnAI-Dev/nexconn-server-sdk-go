# OpenChannelGlobalMuteListAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ParticipantIds** | **[]string** |  | 
**DurationMinutes** | **int32** |  | 
**Extra** | Pointer to **string** | Notification extra payload in JSON string format. | [optional] 
**NeedNotify** | Pointer to **bool** |  | [optional] 

## Methods

### NewOpenChannelGlobalMuteListAddRequest

`func NewOpenChannelGlobalMuteListAddRequest(participantIds []string, durationMinutes int32, ) *OpenChannelGlobalMuteListAddRequest`

NewOpenChannelGlobalMuteListAddRequest instantiates a new OpenChannelGlobalMuteListAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelGlobalMuteListAddRequestWithDefaults

`func NewOpenChannelGlobalMuteListAddRequestWithDefaults() *OpenChannelGlobalMuteListAddRequest`

NewOpenChannelGlobalMuteListAddRequestWithDefaults instantiates a new OpenChannelGlobalMuteListAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetParticipantIds

`func (o *OpenChannelGlobalMuteListAddRequest) GetParticipantIds() []string`

GetParticipantIds returns the ParticipantIds field if non-nil, zero value otherwise.

### GetParticipantIdsOk

`func (o *OpenChannelGlobalMuteListAddRequest) GetParticipantIdsOk() (*[]string, bool)`

GetParticipantIdsOk returns a tuple with the ParticipantIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantIds

`func (o *OpenChannelGlobalMuteListAddRequest) SetParticipantIds(v []string)`

SetParticipantIds sets ParticipantIds field to given value.


### GetDurationMinutes

`func (o *OpenChannelGlobalMuteListAddRequest) GetDurationMinutes() int32`

GetDurationMinutes returns the DurationMinutes field if non-nil, zero value otherwise.

### GetDurationMinutesOk

`func (o *OpenChannelGlobalMuteListAddRequest) GetDurationMinutesOk() (*int32, bool)`

GetDurationMinutesOk returns a tuple with the DurationMinutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDurationMinutes

`func (o *OpenChannelGlobalMuteListAddRequest) SetDurationMinutes(v int32)`

SetDurationMinutes sets DurationMinutes field to given value.


### GetExtra

`func (o *OpenChannelGlobalMuteListAddRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *OpenChannelGlobalMuteListAddRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *OpenChannelGlobalMuteListAddRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *OpenChannelGlobalMuteListAddRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetNeedNotify

`func (o *OpenChannelGlobalMuteListAddRequest) GetNeedNotify() bool`

GetNeedNotify returns the NeedNotify field if non-nil, zero value otherwise.

### GetNeedNotifyOk

`func (o *OpenChannelGlobalMuteListAddRequest) GetNeedNotifyOk() (*bool, bool)`

GetNeedNotifyOk returns a tuple with the NeedNotify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedNotify

`func (o *OpenChannelGlobalMuteListAddRequest) SetNeedNotify(v bool)`

SetNeedNotify sets NeedNotify field to given value.

### HasNeedNotify

`func (o *OpenChannelGlobalMuteListAddRequest) HasNeedNotify() bool`

HasNeedNotify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



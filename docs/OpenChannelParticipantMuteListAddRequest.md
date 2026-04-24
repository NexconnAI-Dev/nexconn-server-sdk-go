# OpenChannelParticipantMuteListAddRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**ParticipantIds** | **[]string** |  | 
**DurationMinutes** | **int32** |  | 
**Extra** | Pointer to **string** | Notification extra payload in JSON string format. | [optional] 
**NeedNotify** | Pointer to **bool** |  | [optional] 

## Methods

### NewOpenChannelParticipantMuteListAddRequest

`func NewOpenChannelParticipantMuteListAddRequest(channelId string, participantIds []string, durationMinutes int32, ) *OpenChannelParticipantMuteListAddRequest`

NewOpenChannelParticipantMuteListAddRequest instantiates a new OpenChannelParticipantMuteListAddRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantMuteListAddRequestWithDefaults

`func NewOpenChannelParticipantMuteListAddRequestWithDefaults() *OpenChannelParticipantMuteListAddRequest`

NewOpenChannelParticipantMuteListAddRequestWithDefaults instantiates a new OpenChannelParticipantMuteListAddRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelParticipantMuteListAddRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelParticipantMuteListAddRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelParticipantMuteListAddRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetParticipantIds

`func (o *OpenChannelParticipantMuteListAddRequest) GetParticipantIds() []string`

GetParticipantIds returns the ParticipantIds field if non-nil, zero value otherwise.

### GetParticipantIdsOk

`func (o *OpenChannelParticipantMuteListAddRequest) GetParticipantIdsOk() (*[]string, bool)`

GetParticipantIdsOk returns a tuple with the ParticipantIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantIds

`func (o *OpenChannelParticipantMuteListAddRequest) SetParticipantIds(v []string)`

SetParticipantIds sets ParticipantIds field to given value.


### GetDurationMinutes

`func (o *OpenChannelParticipantMuteListAddRequest) GetDurationMinutes() int32`

GetDurationMinutes returns the DurationMinutes field if non-nil, zero value otherwise.

### GetDurationMinutesOk

`func (o *OpenChannelParticipantMuteListAddRequest) GetDurationMinutesOk() (*int32, bool)`

GetDurationMinutesOk returns a tuple with the DurationMinutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDurationMinutes

`func (o *OpenChannelParticipantMuteListAddRequest) SetDurationMinutes(v int32)`

SetDurationMinutes sets DurationMinutes field to given value.


### GetExtra

`func (o *OpenChannelParticipantMuteListAddRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *OpenChannelParticipantMuteListAddRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *OpenChannelParticipantMuteListAddRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *OpenChannelParticipantMuteListAddRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetNeedNotify

`func (o *OpenChannelParticipantMuteListAddRequest) GetNeedNotify() bool`

GetNeedNotify returns the NeedNotify field if non-nil, zero value otherwise.

### GetNeedNotifyOk

`func (o *OpenChannelParticipantMuteListAddRequest) GetNeedNotifyOk() (*bool, bool)`

GetNeedNotifyOk returns a tuple with the NeedNotify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedNotify

`func (o *OpenChannelParticipantMuteListAddRequest) SetNeedNotify(v bool)`

SetNeedNotify sets NeedNotify field to given value.

### HasNeedNotify

`func (o *OpenChannelParticipantMuteListAddRequest) HasNeedNotify() bool`

HasNeedNotify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



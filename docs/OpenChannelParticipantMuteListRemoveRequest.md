# OpenChannelParticipantMuteListRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**ParticipantIds** | **[]string** |  | 
**Extra** | Pointer to **string** | Notification extra payload in JSON string format. | [optional] 
**NeedNotify** | Pointer to **bool** |  | [optional] 

## Methods

### NewOpenChannelParticipantMuteListRemoveRequest

`func NewOpenChannelParticipantMuteListRemoveRequest(channelId string, participantIds []string, ) *OpenChannelParticipantMuteListRemoveRequest`

NewOpenChannelParticipantMuteListRemoveRequest instantiates a new OpenChannelParticipantMuteListRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantMuteListRemoveRequestWithDefaults

`func NewOpenChannelParticipantMuteListRemoveRequestWithDefaults() *OpenChannelParticipantMuteListRemoveRequest`

NewOpenChannelParticipantMuteListRemoveRequestWithDefaults instantiates a new OpenChannelParticipantMuteListRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelParticipantMuteListRemoveRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetParticipantIds

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetParticipantIds() []string`

GetParticipantIds returns the ParticipantIds field if non-nil, zero value otherwise.

### GetParticipantIdsOk

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetParticipantIdsOk() (*[]string, bool)`

GetParticipantIdsOk returns a tuple with the ParticipantIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantIds

`func (o *OpenChannelParticipantMuteListRemoveRequest) SetParticipantIds(v []string)`

SetParticipantIds sets ParticipantIds field to given value.


### GetExtra

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetExtra() string`

GetExtra returns the Extra field if non-nil, zero value otherwise.

### GetExtraOk

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetExtraOk() (*string, bool)`

GetExtraOk returns a tuple with the Extra field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExtra

`func (o *OpenChannelParticipantMuteListRemoveRequest) SetExtra(v string)`

SetExtra sets Extra field to given value.

### HasExtra

`func (o *OpenChannelParticipantMuteListRemoveRequest) HasExtra() bool`

HasExtra returns a boolean if a field has been set.

### GetNeedNotify

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetNeedNotify() bool`

GetNeedNotify returns the NeedNotify field if non-nil, zero value otherwise.

### GetNeedNotifyOk

`func (o *OpenChannelParticipantMuteListRemoveRequest) GetNeedNotifyOk() (*bool, bool)`

GetNeedNotifyOk returns a tuple with the NeedNotify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNeedNotify

`func (o *OpenChannelParticipantMuteListRemoveRequest) SetNeedNotify(v bool)`

SetNeedNotify sets NeedNotify field to given value.

### HasNeedNotify

`func (o *OpenChannelParticipantMuteListRemoveRequest) HasNeedNotify() bool`

HasNeedNotify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



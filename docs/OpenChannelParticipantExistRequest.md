# OpenChannelParticipantExistRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | The open channel ID. | 
**ParticipantIds** | **[]string** | User IDs to check. Up to 1,000 users per request. Pass a single-element array to check one user. | 

## Methods

### NewOpenChannelParticipantExistRequest

`func NewOpenChannelParticipantExistRequest(channelId string, participantIds []string, ) *OpenChannelParticipantExistRequest`

NewOpenChannelParticipantExistRequest instantiates a new OpenChannelParticipantExistRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantExistRequestWithDefaults

`func NewOpenChannelParticipantExistRequestWithDefaults() *OpenChannelParticipantExistRequest`

NewOpenChannelParticipantExistRequestWithDefaults instantiates a new OpenChannelParticipantExistRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelParticipantExistRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelParticipantExistRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelParticipantExistRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetParticipantIds

`func (o *OpenChannelParticipantExistRequest) GetParticipantIds() []string`

GetParticipantIds returns the ParticipantIds field if non-nil, zero value otherwise.

### GetParticipantIdsOk

`func (o *OpenChannelParticipantExistRequest) GetParticipantIdsOk() (*[]string, bool)`

GetParticipantIdsOk returns a tuple with the ParticipantIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticipantIds

`func (o *OpenChannelParticipantExistRequest) SetParticipantIds(v []string)`

SetParticipantIds sets ParticipantIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



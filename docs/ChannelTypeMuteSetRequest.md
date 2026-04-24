# ChannelTypeMuteSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserIds** | **[]string** |  | 
**MuteState** | **int32** | &#x60;0&#x60; removes mute and &#x60;1&#x60; enables mute. | 
**ChannelTypes** | **[]string** | Channel types to apply (e.g. &#x60;PERSON&#x60;, &#x60;GROUP&#x60;, &#x60;CHATROOM&#x60;). Server validates against supported enums. | 

## Methods

### NewChannelTypeMuteSetRequest

`func NewChannelTypeMuteSetRequest(userIds []string, muteState int32, channelTypes []string, ) *ChannelTypeMuteSetRequest`

NewChannelTypeMuteSetRequest instantiates a new ChannelTypeMuteSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeMuteSetRequestWithDefaults

`func NewChannelTypeMuteSetRequestWithDefaults() *ChannelTypeMuteSetRequest`

NewChannelTypeMuteSetRequestWithDefaults instantiates a new ChannelTypeMuteSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserIds

`func (o *ChannelTypeMuteSetRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *ChannelTypeMuteSetRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *ChannelTypeMuteSetRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetMuteState

`func (o *ChannelTypeMuteSetRequest) GetMuteState() int32`

GetMuteState returns the MuteState field if non-nil, zero value otherwise.

### GetMuteStateOk

`func (o *ChannelTypeMuteSetRequest) GetMuteStateOk() (*int32, bool)`

GetMuteStateOk returns a tuple with the MuteState field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMuteState

`func (o *ChannelTypeMuteSetRequest) SetMuteState(v int32)`

SetMuteState sets MuteState field to given value.


### GetChannelTypes

`func (o *ChannelTypeMuteSetRequest) GetChannelTypes() []string`

GetChannelTypes returns the ChannelTypes field if non-nil, zero value otherwise.

### GetChannelTypesOk

`func (o *ChannelTypeMuteSetRequest) GetChannelTypesOk() (*[]string, bool)`

GetChannelTypesOk returns a tuple with the ChannelTypes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelTypes

`func (o *ChannelTypeMuteSetRequest) SetChannelTypes(v []string)`

SetChannelTypes sets ChannelTypes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



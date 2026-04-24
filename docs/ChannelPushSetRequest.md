# ChannelPushSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). Matches &#x60;ChannelTypeRequestInput&#x60; in the service. | 
**RequestId** | **string** | User ID whose channel notification setting is updated. | 
**ChannelId** | **string** | Legacy &#x60;targetId&#x60;. | 
**SubchannelId** | Pointer to **string** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. | [optional] 
**NoDisturbLevel** | **int32** | Do-not-disturb level (required by service validation; range &#x60;-1&#x60; to &#x60;5&#x60;). | 

## Methods

### NewChannelPushSetRequest

`func NewChannelPushSetRequest(channelType string, requestId string, channelId string, noDisturbLevel int32, ) *ChannelPushSetRequest`

NewChannelPushSetRequest instantiates a new ChannelPushSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelPushSetRequestWithDefaults

`func NewChannelPushSetRequestWithDefaults() *ChannelPushSetRequest`

NewChannelPushSetRequestWithDefaults instantiates a new ChannelPushSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelType

`func (o *ChannelPushSetRequest) GetChannelType() string`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelPushSetRequest) GetChannelTypeOk() (*string, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelPushSetRequest) SetChannelType(v string)`

SetChannelType sets ChannelType field to given value.


### GetRequestId

`func (o *ChannelPushSetRequest) GetRequestId() string`

GetRequestId returns the RequestId field if non-nil, zero value otherwise.

### GetRequestIdOk

`func (o *ChannelPushSetRequest) GetRequestIdOk() (*string, bool)`

GetRequestIdOk returns a tuple with the RequestId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestId

`func (o *ChannelPushSetRequest) SetRequestId(v string)`

SetRequestId sets RequestId field to given value.


### GetChannelId

`func (o *ChannelPushSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelPushSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelPushSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *ChannelPushSetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *ChannelPushSetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *ChannelPushSetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *ChannelPushSetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetNoDisturbLevel

`func (o *ChannelPushSetRequest) GetNoDisturbLevel() int32`

GetNoDisturbLevel returns the NoDisturbLevel field if non-nil, zero value otherwise.

### GetNoDisturbLevelOk

`func (o *ChannelPushSetRequest) GetNoDisturbLevelOk() (*int32, bool)`

GetNoDisturbLevelOk returns a tuple with the NoDisturbLevel field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNoDisturbLevel

`func (o *ChannelPushSetRequest) SetNoDisturbLevel(v int32)`

SetNoDisturbLevel sets NoDisturbLevel field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



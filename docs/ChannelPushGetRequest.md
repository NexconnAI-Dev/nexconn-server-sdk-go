# ChannelPushGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). | 
**RequestId** | **string** | User ID whose channel notification setting is queried. | 
**ChannelId** | **string** | Legacy &#x60;targetId&#x60;. | 
**SubchannelId** | Pointer to **string** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. | [optional] 

## Methods

### NewChannelPushGetRequest

`func NewChannelPushGetRequest(channelType string, requestId string, channelId string, ) *ChannelPushGetRequest`

NewChannelPushGetRequest instantiates a new ChannelPushGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelPushGetRequestWithDefaults

`func NewChannelPushGetRequestWithDefaults() *ChannelPushGetRequest`

NewChannelPushGetRequestWithDefaults instantiates a new ChannelPushGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelType

`func (o *ChannelPushGetRequest) GetChannelType() string`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelPushGetRequest) GetChannelTypeOk() (*string, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelPushGetRequest) SetChannelType(v string)`

SetChannelType sets ChannelType field to given value.


### GetRequestId

`func (o *ChannelPushGetRequest) GetRequestId() string`

GetRequestId returns the RequestId field if non-nil, zero value otherwise.

### GetRequestIdOk

`func (o *ChannelPushGetRequest) GetRequestIdOk() (*string, bool)`

GetRequestIdOk returns a tuple with the RequestId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestId

`func (o *ChannelPushGetRequest) SetRequestId(v string)`

SetRequestId sets RequestId field to given value.


### GetChannelId

`func (o *ChannelPushGetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelPushGetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelPushGetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *ChannelPushGetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *ChannelPushGetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *ChannelPushGetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *ChannelPushGetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



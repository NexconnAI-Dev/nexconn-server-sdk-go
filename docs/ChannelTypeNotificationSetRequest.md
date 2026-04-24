# ChannelTypeNotificationSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). | 
**RequestId** | **string** | User ID whose channel-type notification setting is updated. | 
**NoDisturbLevel** | **int32** | Do-not-disturb level for the specified channel type. | 

## Methods

### NewChannelTypeNotificationSetRequest

`func NewChannelTypeNotificationSetRequest(channelType string, requestId string, noDisturbLevel int32, ) *ChannelTypeNotificationSetRequest`

NewChannelTypeNotificationSetRequest instantiates a new ChannelTypeNotificationSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeNotificationSetRequestWithDefaults

`func NewChannelTypeNotificationSetRequestWithDefaults() *ChannelTypeNotificationSetRequest`

NewChannelTypeNotificationSetRequestWithDefaults instantiates a new ChannelTypeNotificationSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelType

`func (o *ChannelTypeNotificationSetRequest) GetChannelType() string`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelTypeNotificationSetRequest) GetChannelTypeOk() (*string, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelTypeNotificationSetRequest) SetChannelType(v string)`

SetChannelType sets ChannelType field to given value.


### GetRequestId

`func (o *ChannelTypeNotificationSetRequest) GetRequestId() string`

GetRequestId returns the RequestId field if non-nil, zero value otherwise.

### GetRequestIdOk

`func (o *ChannelTypeNotificationSetRequest) GetRequestIdOk() (*string, bool)`

GetRequestIdOk returns a tuple with the RequestId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestId

`func (o *ChannelTypeNotificationSetRequest) SetRequestId(v string)`

SetRequestId sets RequestId field to given value.


### GetNoDisturbLevel

`func (o *ChannelTypeNotificationSetRequest) GetNoDisturbLevel() int32`

GetNoDisturbLevel returns the NoDisturbLevel field if non-nil, zero value otherwise.

### GetNoDisturbLevelOk

`func (o *ChannelTypeNotificationSetRequest) GetNoDisturbLevelOk() (*int32, bool)`

GetNoDisturbLevelOk returns a tuple with the NoDisturbLevel field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNoDisturbLevel

`func (o *ChannelTypeNotificationSetRequest) SetNoDisturbLevel(v int32)`

SetNoDisturbLevel sets NoDisturbLevel field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



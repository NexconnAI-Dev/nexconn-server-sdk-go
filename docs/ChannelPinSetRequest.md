# ChannelPinSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**ChannelType** | **int32** | Legacy &#x60;conversationType&#x60;. Current docs use numeric channel types such as &#x60;1&#x60;, &#x60;3&#x60;, and &#x60;6&#x60;. | 
**ChannelId** | **string** | Legacy &#x60;targetId&#x60;. | 
**IsPin** | **bool** | JSON field name used by the server. &#x60;true&#x60; pins the conversation and &#x60;false&#x60; cancels the pin. | 

## Methods

### NewChannelPinSetRequest

`func NewChannelPinSetRequest(userId string, channelType int32, channelId string, isPin bool, ) *ChannelPinSetRequest`

NewChannelPinSetRequest instantiates a new ChannelPinSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelPinSetRequestWithDefaults

`func NewChannelPinSetRequestWithDefaults() *ChannelPinSetRequest`

NewChannelPinSetRequestWithDefaults instantiates a new ChannelPinSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *ChannelPinSetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *ChannelPinSetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *ChannelPinSetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelType

`func (o *ChannelPinSetRequest) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelPinSetRequest) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelPinSetRequest) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.


### GetChannelId

`func (o *ChannelPinSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelPinSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelPinSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetIsPin

`func (o *ChannelPinSetRequest) GetIsPin() bool`

GetIsPin returns the IsPin field if non-nil, zero value otherwise.

### GetIsPinOk

`func (o *ChannelPinSetRequest) GetIsPinOk() (*bool, bool)`

GetIsPinOk returns a tuple with the IsPin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIsPin

`func (o *ChannelPinSetRequest) SetIsPin(v bool)`

SetIsPin sets IsPin field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



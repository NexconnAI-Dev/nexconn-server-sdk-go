# ChannelAttributeGetResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** |  | [optional] 
**ChannelType** | Pointer to **int32** |  | [optional] 
**Pin** | Pointer to [**ChannelPinState**](ChannelPinState.md) |  | [optional] 
**Notification** | Pointer to [**ChannelNotificationState**](ChannelNotificationState.md) |  | [optional] 
**Tags** | Pointer to [**[]ChannelAttributeTagItem**](ChannelAttributeTagItem.md) | Same shape as &#x60;ChannelAttributeResult.TagInfo&#x60; (no &#x60;createdAt&#x60;; distinct from user tag list items). | [optional] 

## Methods

### NewChannelAttributeGetResponseResult

`func NewChannelAttributeGetResponseResult() *ChannelAttributeGetResponseResult`

NewChannelAttributeGetResponseResult instantiates a new ChannelAttributeGetResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelAttributeGetResponseResultWithDefaults

`func NewChannelAttributeGetResponseResultWithDefaults() *ChannelAttributeGetResponseResult`

NewChannelAttributeGetResponseResultWithDefaults instantiates a new ChannelAttributeGetResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *ChannelAttributeGetResponseResult) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *ChannelAttributeGetResponseResult) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *ChannelAttributeGetResponseResult) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *ChannelAttributeGetResponseResult) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetChannelType

`func (o *ChannelAttributeGetResponseResult) GetChannelType() int32`

GetChannelType returns the ChannelType field if non-nil, zero value otherwise.

### GetChannelTypeOk

`func (o *ChannelAttributeGetResponseResult) GetChannelTypeOk() (*int32, bool)`

GetChannelTypeOk returns a tuple with the ChannelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelType

`func (o *ChannelAttributeGetResponseResult) SetChannelType(v int32)`

SetChannelType sets ChannelType field to given value.

### HasChannelType

`func (o *ChannelAttributeGetResponseResult) HasChannelType() bool`

HasChannelType returns a boolean if a field has been set.

### GetPin

`func (o *ChannelAttributeGetResponseResult) GetPin() ChannelPinState`

GetPin returns the Pin field if non-nil, zero value otherwise.

### GetPinOk

`func (o *ChannelAttributeGetResponseResult) GetPinOk() (*ChannelPinState, bool)`

GetPinOk returns a tuple with the Pin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPin

`func (o *ChannelAttributeGetResponseResult) SetPin(v ChannelPinState)`

SetPin sets Pin field to given value.

### HasPin

`func (o *ChannelAttributeGetResponseResult) HasPin() bool`

HasPin returns a boolean if a field has been set.

### GetNotification

`func (o *ChannelAttributeGetResponseResult) GetNotification() ChannelNotificationState`

GetNotification returns the Notification field if non-nil, zero value otherwise.

### GetNotificationOk

`func (o *ChannelAttributeGetResponseResult) GetNotificationOk() (*ChannelNotificationState, bool)`

GetNotificationOk returns a tuple with the Notification field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNotification

`func (o *ChannelAttributeGetResponseResult) SetNotification(v ChannelNotificationState)`

SetNotification sets Notification field to given value.

### HasNotification

`func (o *ChannelAttributeGetResponseResult) HasNotification() bool`

HasNotification returns a boolean if a field has been set.

### GetTags

`func (o *ChannelAttributeGetResponseResult) GetTags() []ChannelAttributeTagItem`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *ChannelAttributeGetResponseResult) GetTagsOk() (*[]ChannelAttributeTagItem, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *ChannelAttributeGetResponseResult) SetTags(v []ChannelAttributeTagItem)`

SetTags sets Tags field to given value.

### HasTags

`func (o *ChannelAttributeGetResponseResult) HasTags() bool`

HasTags returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# SystemChannelPushRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **[]string** |  | 
**FromUserId** | **string** |  | 
**Audience** | [**SystemChannelPushAudience**](SystemChannelPushAudience.md) |  | 
**Message** | [**SystemChannelPushMessage**](SystemChannelPushMessage.md) |  | 
**Notification** | [**SystemChannelPushNotification**](SystemChannelPushNotification.md) |  | 

## Methods

### NewSystemChannelPushRequest

`func NewSystemChannelPushRequest(platform []string, fromUserId string, audience SystemChannelPushAudience, message SystemChannelPushMessage, notification SystemChannelPushNotification, ) *SystemChannelPushRequest`

NewSystemChannelPushRequest instantiates a new SystemChannelPushRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSystemChannelPushRequestWithDefaults

`func NewSystemChannelPushRequestWithDefaults() *SystemChannelPushRequest`

NewSystemChannelPushRequestWithDefaults instantiates a new SystemChannelPushRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPlatform

`func (o *SystemChannelPushRequest) GetPlatform() []string`

GetPlatform returns the Platform field if non-nil, zero value otherwise.

### GetPlatformOk

`func (o *SystemChannelPushRequest) GetPlatformOk() (*[]string, bool)`

GetPlatformOk returns a tuple with the Platform field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlatform

`func (o *SystemChannelPushRequest) SetPlatform(v []string)`

SetPlatform sets Platform field to given value.


### GetFromUserId

`func (o *SystemChannelPushRequest) GetFromUserId() string`

GetFromUserId returns the FromUserId field if non-nil, zero value otherwise.

### GetFromUserIdOk

`func (o *SystemChannelPushRequest) GetFromUserIdOk() (*string, bool)`

GetFromUserIdOk returns a tuple with the FromUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromUserId

`func (o *SystemChannelPushRequest) SetFromUserId(v string)`

SetFromUserId sets FromUserId field to given value.


### GetAudience

`func (o *SystemChannelPushRequest) GetAudience() SystemChannelPushAudience`

GetAudience returns the Audience field if non-nil, zero value otherwise.

### GetAudienceOk

`func (o *SystemChannelPushRequest) GetAudienceOk() (*SystemChannelPushAudience, bool)`

GetAudienceOk returns a tuple with the Audience field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAudience

`func (o *SystemChannelPushRequest) SetAudience(v SystemChannelPushAudience)`

SetAudience sets Audience field to given value.


### GetMessage

`func (o *SystemChannelPushRequest) GetMessage() SystemChannelPushMessage`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *SystemChannelPushRequest) GetMessageOk() (*SystemChannelPushMessage, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *SystemChannelPushRequest) SetMessage(v SystemChannelPushMessage)`

SetMessage sets Message field to given value.


### GetNotification

`func (o *SystemChannelPushRequest) GetNotification() SystemChannelPushNotification`

GetNotification returns the Notification field if non-nil, zero value otherwise.

### GetNotificationOk

`func (o *SystemChannelPushRequest) GetNotificationOk() (*SystemChannelPushNotification, bool)`

GetNotificationOk returns a tuple with the Notification field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNotification

`func (o *SystemChannelPushRequest) SetNotification(v SystemChannelPushNotification)`

SetNotification sets Notification field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



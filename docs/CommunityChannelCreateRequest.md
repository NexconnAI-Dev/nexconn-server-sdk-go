# CommunityChannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** | Initial member to join after community creation. | 
**ChannelId** | **string** | Legacy &#x60;groupId&#x60;. | 
**Name** | **string** |  | 

## Methods

### NewCommunityChannelCreateRequest

`func NewCommunityChannelCreateRequest(userId string, channelId string, name string, ) *CommunityChannelCreateRequest`

NewCommunityChannelCreateRequest instantiates a new CommunityChannelCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelCreateRequestWithDefaults

`func NewCommunityChannelCreateRequestWithDefaults() *CommunityChannelCreateRequest`

NewCommunityChannelCreateRequestWithDefaults instantiates a new CommunityChannelCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *CommunityChannelCreateRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityChannelCreateRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityChannelCreateRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetChannelId

`func (o *CommunityChannelCreateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelCreateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelCreateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetName

`func (o *CommunityChannelCreateRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *CommunityChannelCreateRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *CommunityChannelCreateRequest) SetName(v string)`

SetName sets Name field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



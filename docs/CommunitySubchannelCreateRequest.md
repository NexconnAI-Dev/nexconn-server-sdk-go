# CommunitySubchannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | **string** | Legacy &#x60;busChannel&#x60;. | 
**ChannelVisibility** | Pointer to **int32** | Legacy &#x60;type&#x60;. &#x60;0&#x60; for public and &#x60;1&#x60; for private. | [optional] 

## Methods

### NewCommunitySubchannelCreateRequest

`func NewCommunitySubchannelCreateRequest(channelId string, subchannelId string, ) *CommunitySubchannelCreateRequest`

NewCommunitySubchannelCreateRequest instantiates a new CommunitySubchannelCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunitySubchannelCreateRequestWithDefaults

`func NewCommunitySubchannelCreateRequestWithDefaults() *CommunitySubchannelCreateRequest`

NewCommunitySubchannelCreateRequestWithDefaults instantiates a new CommunitySubchannelCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunitySubchannelCreateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunitySubchannelCreateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunitySubchannelCreateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunitySubchannelCreateRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunitySubchannelCreateRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunitySubchannelCreateRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.


### GetChannelVisibility

`func (o *CommunitySubchannelCreateRequest) GetChannelVisibility() int32`

GetChannelVisibility returns the ChannelVisibility field if non-nil, zero value otherwise.

### GetChannelVisibilityOk

`func (o *CommunitySubchannelCreateRequest) GetChannelVisibilityOk() (*int32, bool)`

GetChannelVisibilityOk returns a tuple with the ChannelVisibility field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelVisibility

`func (o *CommunitySubchannelCreateRequest) SetChannelVisibility(v int32)`

SetChannelVisibility sets ChannelVisibility field to given value.

### HasChannelVisibility

`func (o *CommunitySubchannelCreateRequest) HasChannelVisibility() bool`

HasChannelVisibility returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



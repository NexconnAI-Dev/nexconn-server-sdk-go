# CommunitySubchannelTypeUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | **string** |  | 
**ChannelVisibility** | Pointer to **int32** | &#39;0&#39; for public and &#39;1&#39; for private. | [optional] 

## Methods

### NewCommunitySubchannelTypeUpdateRequest

`func NewCommunitySubchannelTypeUpdateRequest(channelId string, subchannelId string, ) *CommunitySubchannelTypeUpdateRequest`

NewCommunitySubchannelTypeUpdateRequest instantiates a new CommunitySubchannelTypeUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunitySubchannelTypeUpdateRequestWithDefaults

`func NewCommunitySubchannelTypeUpdateRequestWithDefaults() *CommunitySubchannelTypeUpdateRequest`

NewCommunitySubchannelTypeUpdateRequestWithDefaults instantiates a new CommunitySubchannelTypeUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunitySubchannelTypeUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunitySubchannelTypeUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunitySubchannelTypeUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunitySubchannelTypeUpdateRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunitySubchannelTypeUpdateRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunitySubchannelTypeUpdateRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.


### GetChannelVisibility

`func (o *CommunitySubchannelTypeUpdateRequest) GetChannelVisibility() int32`

GetChannelVisibility returns the ChannelVisibility field if non-nil, zero value otherwise.

### GetChannelVisibilityOk

`func (o *CommunitySubchannelTypeUpdateRequest) GetChannelVisibilityOk() (*int32, bool)`

GetChannelVisibilityOk returns a tuple with the ChannelVisibility field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelVisibility

`func (o *CommunitySubchannelTypeUpdateRequest) SetChannelVisibility(v int32)`

SetChannelVisibility sets ChannelVisibility field to given value.

### HasChannelVisibility

`func (o *CommunitySubchannelTypeUpdateRequest) HasChannelVisibility() bool`

HasChannelVisibility returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



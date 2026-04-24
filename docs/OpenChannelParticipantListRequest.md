# OpenChannelParticipantListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**PageSize** | Pointer to **int32** |  | [optional] 
**Order** | Pointer to **int32** | &#x60;1&#x60; for ascending join time and &#x60;2&#x60; for descending join time. | [optional] 

## Methods

### NewOpenChannelParticipantListRequest

`func NewOpenChannelParticipantListRequest(channelId string, ) *OpenChannelParticipantListRequest`

NewOpenChannelParticipantListRequest instantiates a new OpenChannelParticipantListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelParticipantListRequestWithDefaults

`func NewOpenChannelParticipantListRequestWithDefaults() *OpenChannelParticipantListRequest`

NewOpenChannelParticipantListRequestWithDefaults instantiates a new OpenChannelParticipantListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelParticipantListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelParticipantListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelParticipantListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetPageSize

`func (o *OpenChannelParticipantListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *OpenChannelParticipantListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *OpenChannelParticipantListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *OpenChannelParticipantListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *OpenChannelParticipantListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *OpenChannelParticipantListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *OpenChannelParticipantListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *OpenChannelParticipantListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



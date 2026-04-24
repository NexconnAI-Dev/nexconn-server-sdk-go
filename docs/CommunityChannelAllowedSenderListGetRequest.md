# CommunityChannelAllowedSenderListGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**Page** | Pointer to **int32** |  | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 50]

## Methods

### NewCommunityChannelAllowedSenderListGetRequest

`func NewCommunityChannelAllowedSenderListGetRequest(channelId string, ) *CommunityChannelAllowedSenderListGetRequest`

NewCommunityChannelAllowedSenderListGetRequest instantiates a new CommunityChannelAllowedSenderListGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelAllowedSenderListGetRequestWithDefaults

`func NewCommunityChannelAllowedSenderListGetRequestWithDefaults() *CommunityChannelAllowedSenderListGetRequest`

NewCommunityChannelAllowedSenderListGetRequestWithDefaults instantiates a new CommunityChannelAllowedSenderListGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelAllowedSenderListGetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelAllowedSenderListGetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelAllowedSenderListGetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelAllowedSenderListGetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelAllowedSenderListGetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelAllowedSenderListGetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelAllowedSenderListGetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetPage

`func (o *CommunityChannelAllowedSenderListGetRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityChannelAllowedSenderListGetRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityChannelAllowedSenderListGetRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityChannelAllowedSenderListGetRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityChannelAllowedSenderListGetRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityChannelAllowedSenderListGetRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityChannelAllowedSenderListGetRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityChannelAllowedSenderListGetRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



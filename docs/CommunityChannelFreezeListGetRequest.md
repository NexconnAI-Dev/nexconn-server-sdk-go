# CommunityChannelFreezeListGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** |  | [optional] 
**Page** | Pointer to **int32** | Pagination field from &#x60;CommunityAllowedSenderListInput&#x60; / &#x60;AbstractCommunityPagingInput&#x60; (present in Java model; not all server code paths consume it). | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 50]

## Methods

### NewCommunityChannelFreezeListGetRequest

`func NewCommunityChannelFreezeListGetRequest(channelId string, ) *CommunityChannelFreezeListGetRequest`

NewCommunityChannelFreezeListGetRequest instantiates a new CommunityChannelFreezeListGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelFreezeListGetRequestWithDefaults

`func NewCommunityChannelFreezeListGetRequestWithDefaults() *CommunityChannelFreezeListGetRequest`

NewCommunityChannelFreezeListGetRequestWithDefaults instantiates a new CommunityChannelFreezeListGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelFreezeListGetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelFreezeListGetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelFreezeListGetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelFreezeListGetRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelFreezeListGetRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelFreezeListGetRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelFreezeListGetRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetPage

`func (o *CommunityChannelFreezeListGetRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityChannelFreezeListGetRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityChannelFreezeListGetRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityChannelFreezeListGetRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityChannelFreezeListGetRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityChannelFreezeListGetRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityChannelFreezeListGetRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityChannelFreezeListGetRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



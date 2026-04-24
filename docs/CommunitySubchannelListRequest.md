# CommunitySubchannelListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**Page** | Pointer to **int32** |  | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 20]
**Order** | Pointer to **int32** | Sort order from &#x60;CommunityChannelPageInput&#x60;. | [optional] 

## Methods

### NewCommunitySubchannelListRequest

`func NewCommunitySubchannelListRequest(channelId string, ) *CommunitySubchannelListRequest`

NewCommunitySubchannelListRequest instantiates a new CommunitySubchannelListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunitySubchannelListRequestWithDefaults

`func NewCommunitySubchannelListRequestWithDefaults() *CommunitySubchannelListRequest`

NewCommunitySubchannelListRequestWithDefaults instantiates a new CommunitySubchannelListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunitySubchannelListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunitySubchannelListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunitySubchannelListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetPage

`func (o *CommunitySubchannelListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunitySubchannelListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunitySubchannelListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunitySubchannelListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunitySubchannelListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunitySubchannelListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunitySubchannelListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunitySubchannelListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *CommunitySubchannelListRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *CommunitySubchannelListRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *CommunitySubchannelListRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *CommunitySubchannelListRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



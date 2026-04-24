# CommunityUserSubchannelListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserId** | **string** |  | 
**Page** | Pointer to **int32** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] [default to 10]

## Methods

### NewCommunityUserSubchannelListRequest

`func NewCommunityUserSubchannelListRequest(channelId string, userId string, ) *CommunityUserSubchannelListRequest`

NewCommunityUserSubchannelListRequest instantiates a new CommunityUserSubchannelListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityUserSubchannelListRequestWithDefaults

`func NewCommunityUserSubchannelListRequestWithDefaults() *CommunityUserSubchannelListRequest`

NewCommunityUserSubchannelListRequestWithDefaults instantiates a new CommunityUserSubchannelListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityUserSubchannelListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityUserSubchannelListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityUserSubchannelListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserId

`func (o *CommunityUserSubchannelListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityUserSubchannelListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityUserSubchannelListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetPage

`func (o *CommunityUserSubchannelListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityUserSubchannelListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityUserSubchannelListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityUserSubchannelListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityUserSubchannelListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityUserSubchannelListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityUserSubchannelListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityUserSubchannelListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



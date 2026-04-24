# CommunityChannelUserUserGroupListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**UserId** | **string** |  | 
**Page** | Pointer to **int32** |  | [optional] [default to 1]
**PageSize** | Pointer to **int32** |  | [optional] [default to 10]

## Methods

### NewCommunityChannelUserUserGroupListRequest

`func NewCommunityChannelUserUserGroupListRequest(channelId string, userId string, ) *CommunityChannelUserUserGroupListRequest`

NewCommunityChannelUserUserGroupListRequest instantiates a new CommunityChannelUserUserGroupListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelUserUserGroupListRequestWithDefaults

`func NewCommunityChannelUserUserGroupListRequestWithDefaults() *CommunityChannelUserUserGroupListRequest`

NewCommunityChannelUserUserGroupListRequestWithDefaults instantiates a new CommunityChannelUserUserGroupListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *CommunityChannelUserUserGroupListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelUserUserGroupListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelUserUserGroupListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetUserId

`func (o *CommunityChannelUserUserGroupListRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *CommunityChannelUserUserGroupListRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *CommunityChannelUserUserGroupListRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetPage

`func (o *CommunityChannelUserUserGroupListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityChannelUserUserGroupListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityChannelUserUserGroupListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityChannelUserUserGroupListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.

### GetPageSize

`func (o *CommunityChannelUserUserGroupListRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *CommunityChannelUserUserGroupListRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *CommunityChannelUserUserGroupListRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *CommunityChannelUserUserGroupListRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# CommunityChannelMessageMetadataListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**ChannelId** | **string** |  | 
**SubchannelId** | Pointer to **string** | Should match the subchannel used when the message was sent. | [optional] 
**Page** | Pointer to **int32** |  | [optional] 

## Methods

### NewCommunityChannelMessageMetadataListRequest

`func NewCommunityChannelMessageMetadataListRequest(messageId string, channelId string, ) *CommunityChannelMessageMetadataListRequest`

NewCommunityChannelMessageMetadataListRequest instantiates a new CommunityChannelMessageMetadataListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageMetadataListRequestWithDefaults

`func NewCommunityChannelMessageMetadataListRequestWithDefaults() *CommunityChannelMessageMetadataListRequest`

NewCommunityChannelMessageMetadataListRequestWithDefaults instantiates a new CommunityChannelMessageMetadataListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *CommunityChannelMessageMetadataListRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *CommunityChannelMessageMetadataListRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *CommunityChannelMessageMetadataListRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetChannelId

`func (o *CommunityChannelMessageMetadataListRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *CommunityChannelMessageMetadataListRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *CommunityChannelMessageMetadataListRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetSubchannelId

`func (o *CommunityChannelMessageMetadataListRequest) GetSubchannelId() string`

GetSubchannelId returns the SubchannelId field if non-nil, zero value otherwise.

### GetSubchannelIdOk

`func (o *CommunityChannelMessageMetadataListRequest) GetSubchannelIdOk() (*string, bool)`

GetSubchannelIdOk returns a tuple with the SubchannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannelId

`func (o *CommunityChannelMessageMetadataListRequest) SetSubchannelId(v string)`

SetSubchannelId sets SubchannelId field to given value.

### HasSubchannelId

`func (o *CommunityChannelMessageMetadataListRequest) HasSubchannelId() bool`

HasSubchannelId returns a boolean if a field has been set.

### GetPage

`func (o *CommunityChannelMessageMetadataListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *CommunityChannelMessageMetadataListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *CommunityChannelMessageMetadataListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *CommunityChannelMessageMetadataListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ChannelTypeMessageMetadataListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | 
**Page** | Pointer to **int32** |  | [optional] 

## Methods

### NewChannelTypeMessageMetadataListRequest

`func NewChannelTypeMessageMetadataListRequest(messageId string, ) *ChannelTypeMessageMetadataListRequest`

NewChannelTypeMessageMetadataListRequest instantiates a new ChannelTypeMessageMetadataListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewChannelTypeMessageMetadataListRequestWithDefaults

`func NewChannelTypeMessageMetadataListRequestWithDefaults() *ChannelTypeMessageMetadataListRequest`

NewChannelTypeMessageMetadataListRequestWithDefaults instantiates a new ChannelTypeMessageMetadataListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMessageId

`func (o *ChannelTypeMessageMetadataListRequest) GetMessageId() string`

GetMessageId returns the MessageId field if non-nil, zero value otherwise.

### GetMessageIdOk

`func (o *ChannelTypeMessageMetadataListRequest) GetMessageIdOk() (*string, bool)`

GetMessageIdOk returns a tuple with the MessageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessageId

`func (o *ChannelTypeMessageMetadataListRequest) SetMessageId(v string)`

SetMessageId sets MessageId field to given value.


### GetPage

`func (o *ChannelTypeMessageMetadataListRequest) GetPage() int32`

GetPage returns the Page field if non-nil, zero value otherwise.

### GetPageOk

`func (o *ChannelTypeMessageMetadataListRequest) GetPageOk() (*int32, bool)`

GetPageOk returns a tuple with the Page field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPage

`func (o *ChannelTypeMessageMetadataListRequest) SetPage(v int32)`

SetPage sets Page field to given value.

### HasPage

`func (o *ChannelTypeMessageMetadataListRequest) HasPage() bool`

HasPage returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



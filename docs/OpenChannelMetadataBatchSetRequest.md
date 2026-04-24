# OpenChannelMetadataBatchSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**MetadataOwnerId** | **string** | Legacy &#x60;entryOwnerId&#x60;. | 
**Metadata** | **map[string]string** | Legacy &#x60;entryInfo&#x60;. Up to 20 metadata entries per request. | 
**ShouldAutoDelete** | Pointer to **int32** | &#x60;0&#x60; keeps metadata after the owner leaves and &#x60;1&#x60; removes it automatically. | [optional] 

## Methods

### NewOpenChannelMetadataBatchSetRequest

`func NewOpenChannelMetadataBatchSetRequest(channelId string, metadataOwnerId string, metadata map[string]string, ) *OpenChannelMetadataBatchSetRequest`

NewOpenChannelMetadataBatchSetRequest instantiates a new OpenChannelMetadataBatchSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMetadataBatchSetRequestWithDefaults

`func NewOpenChannelMetadataBatchSetRequestWithDefaults() *OpenChannelMetadataBatchSetRequest`

NewOpenChannelMetadataBatchSetRequestWithDefaults instantiates a new OpenChannelMetadataBatchSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelMetadataBatchSetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelMetadataBatchSetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelMetadataBatchSetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetMetadataOwnerId

`func (o *OpenChannelMetadataBatchSetRequest) GetMetadataOwnerId() string`

GetMetadataOwnerId returns the MetadataOwnerId field if non-nil, zero value otherwise.

### GetMetadataOwnerIdOk

`func (o *OpenChannelMetadataBatchSetRequest) GetMetadataOwnerIdOk() (*string, bool)`

GetMetadataOwnerIdOk returns a tuple with the MetadataOwnerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataOwnerId

`func (o *OpenChannelMetadataBatchSetRequest) SetMetadataOwnerId(v string)`

SetMetadataOwnerId sets MetadataOwnerId field to given value.


### GetMetadata

`func (o *OpenChannelMetadataBatchSetRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *OpenChannelMetadataBatchSetRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *OpenChannelMetadataBatchSetRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.


### GetShouldAutoDelete

`func (o *OpenChannelMetadataBatchSetRequest) GetShouldAutoDelete() int32`

GetShouldAutoDelete returns the ShouldAutoDelete field if non-nil, zero value otherwise.

### GetShouldAutoDeleteOk

`func (o *OpenChannelMetadataBatchSetRequest) GetShouldAutoDeleteOk() (*int32, bool)`

GetShouldAutoDeleteOk returns a tuple with the ShouldAutoDelete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldAutoDelete

`func (o *OpenChannelMetadataBatchSetRequest) SetShouldAutoDelete(v int32)`

SetShouldAutoDelete sets ShouldAutoDelete field to given value.

### HasShouldAutoDelete

`func (o *OpenChannelMetadataBatchSetRequest) HasShouldAutoDelete() bool`

HasShouldAutoDelete returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# OpenChannelMetadataBatchGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**MetadataKeys** | Pointer to **[]string** | Metadata keys to fetch. When omitted, the service returns metadata according to its default rule. | [optional] 

## Methods

### NewOpenChannelMetadataBatchGetRequest

`func NewOpenChannelMetadataBatchGetRequest(channelId string, ) *OpenChannelMetadataBatchGetRequest`

NewOpenChannelMetadataBatchGetRequest instantiates a new OpenChannelMetadataBatchGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMetadataBatchGetRequestWithDefaults

`func NewOpenChannelMetadataBatchGetRequestWithDefaults() *OpenChannelMetadataBatchGetRequest`

NewOpenChannelMetadataBatchGetRequestWithDefaults instantiates a new OpenChannelMetadataBatchGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelMetadataBatchGetRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelMetadataBatchGetRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelMetadataBatchGetRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetMetadataKeys

`func (o *OpenChannelMetadataBatchGetRequest) GetMetadataKeys() []string`

GetMetadataKeys returns the MetadataKeys field if non-nil, zero value otherwise.

### GetMetadataKeysOk

`func (o *OpenChannelMetadataBatchGetRequest) GetMetadataKeysOk() (*[]string, bool)`

GetMetadataKeysOk returns a tuple with the MetadataKeys field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataKeys

`func (o *OpenChannelMetadataBatchGetRequest) SetMetadataKeys(v []string)`

SetMetadataKeys sets MetadataKeys field to given value.

### HasMetadataKeys

`func (o *OpenChannelMetadataBatchGetRequest) HasMetadataKeys() bool`

HasMetadataKeys returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



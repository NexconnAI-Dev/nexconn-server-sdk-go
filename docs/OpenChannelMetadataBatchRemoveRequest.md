# OpenChannelMetadataBatchRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** |  | 
**MetadataOwnerId** | **string** | Legacy &#x60;entryOwnerId&#x60;. | 
**MetadataKeys** | **[]string** |  | 

## Methods

### NewOpenChannelMetadataBatchRemoveRequest

`func NewOpenChannelMetadataBatchRemoveRequest(channelId string, metadataOwnerId string, metadataKeys []string, ) *OpenChannelMetadataBatchRemoveRequest`

NewOpenChannelMetadataBatchRemoveRequest instantiates a new OpenChannelMetadataBatchRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMetadataBatchRemoveRequestWithDefaults

`func NewOpenChannelMetadataBatchRemoveRequestWithDefaults() *OpenChannelMetadataBatchRemoveRequest`

NewOpenChannelMetadataBatchRemoveRequestWithDefaults instantiates a new OpenChannelMetadataBatchRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelMetadataBatchRemoveRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelMetadataBatchRemoveRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelMetadataBatchRemoveRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetMetadataOwnerId

`func (o *OpenChannelMetadataBatchRemoveRequest) GetMetadataOwnerId() string`

GetMetadataOwnerId returns the MetadataOwnerId field if non-nil, zero value otherwise.

### GetMetadataOwnerIdOk

`func (o *OpenChannelMetadataBatchRemoveRequest) GetMetadataOwnerIdOk() (*string, bool)`

GetMetadataOwnerIdOk returns a tuple with the MetadataOwnerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataOwnerId

`func (o *OpenChannelMetadataBatchRemoveRequest) SetMetadataOwnerId(v string)`

SetMetadataOwnerId sets MetadataOwnerId field to given value.


### GetMetadataKeys

`func (o *OpenChannelMetadataBatchRemoveRequest) GetMetadataKeys() []string`

GetMetadataKeys returns the MetadataKeys field if non-nil, zero value otherwise.

### GetMetadataKeysOk

`func (o *OpenChannelMetadataBatchRemoveRequest) GetMetadataKeysOk() (*[]string, bool)`

GetMetadataKeysOk returns a tuple with the MetadataKeys field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataKeys

`func (o *OpenChannelMetadataBatchRemoveRequest) SetMetadataKeys(v []string)`

SetMetadataKeys sets MetadataKeys field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



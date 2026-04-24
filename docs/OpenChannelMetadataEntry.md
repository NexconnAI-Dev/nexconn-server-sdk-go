# OpenChannelMetadataEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | Pointer to **string** |  | [optional] 
**Value** | Pointer to **string** |  | [optional] 
**MetadataOwnerId** | Pointer to **string** | KV entry owner; serializes as &#x60;metadataOwnerId&#x60; from the source map key &#x60;userId&#x60; (&#x60;OpenChannelMetadataListResult.MetadataItem&#x60;). | [optional] 
**ShouldAutoDelete** | Pointer to **int32** | Parsed from source &#x60;autoDelete&#x60; string. &#x60;1&#x60; enables auto-delete and &#x60;0&#x60; disables it. | [optional] 
**UpdatedAt** | Pointer to **int64** | Parsed from source &#x60;lastSetTime&#x60; (milliseconds). | [optional] 

## Methods

### NewOpenChannelMetadataEntry

`func NewOpenChannelMetadataEntry() *OpenChannelMetadataEntry`

NewOpenChannelMetadataEntry instantiates a new OpenChannelMetadataEntry object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelMetadataEntryWithDefaults

`func NewOpenChannelMetadataEntryWithDefaults() *OpenChannelMetadataEntry`

NewOpenChannelMetadataEntryWithDefaults instantiates a new OpenChannelMetadataEntry object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKey

`func (o *OpenChannelMetadataEntry) GetKey() string`

GetKey returns the Key field if non-nil, zero value otherwise.

### GetKeyOk

`func (o *OpenChannelMetadataEntry) GetKeyOk() (*string, bool)`

GetKeyOk returns a tuple with the Key field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKey

`func (o *OpenChannelMetadataEntry) SetKey(v string)`

SetKey sets Key field to given value.

### HasKey

`func (o *OpenChannelMetadataEntry) HasKey() bool`

HasKey returns a boolean if a field has been set.

### GetValue

`func (o *OpenChannelMetadataEntry) GetValue() string`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *OpenChannelMetadataEntry) GetValueOk() (*string, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *OpenChannelMetadataEntry) SetValue(v string)`

SetValue sets Value field to given value.

### HasValue

`func (o *OpenChannelMetadataEntry) HasValue() bool`

HasValue returns a boolean if a field has been set.

### GetMetadataOwnerId

`func (o *OpenChannelMetadataEntry) GetMetadataOwnerId() string`

GetMetadataOwnerId returns the MetadataOwnerId field if non-nil, zero value otherwise.

### GetMetadataOwnerIdOk

`func (o *OpenChannelMetadataEntry) GetMetadataOwnerIdOk() (*string, bool)`

GetMetadataOwnerIdOk returns a tuple with the MetadataOwnerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataOwnerId

`func (o *OpenChannelMetadataEntry) SetMetadataOwnerId(v string)`

SetMetadataOwnerId sets MetadataOwnerId field to given value.

### HasMetadataOwnerId

`func (o *OpenChannelMetadataEntry) HasMetadataOwnerId() bool`

HasMetadataOwnerId returns a boolean if a field has been set.

### GetShouldAutoDelete

`func (o *OpenChannelMetadataEntry) GetShouldAutoDelete() int32`

GetShouldAutoDelete returns the ShouldAutoDelete field if non-nil, zero value otherwise.

### GetShouldAutoDeleteOk

`func (o *OpenChannelMetadataEntry) GetShouldAutoDeleteOk() (*int32, bool)`

GetShouldAutoDeleteOk returns a tuple with the ShouldAutoDelete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldAutoDelete

`func (o *OpenChannelMetadataEntry) SetShouldAutoDelete(v int32)`

SetShouldAutoDelete sets ShouldAutoDelete field to given value.

### HasShouldAutoDelete

`func (o *OpenChannelMetadataEntry) HasShouldAutoDelete() bool`

HasShouldAutoDelete returns a boolean if a field has been set.

### GetUpdatedAt

`func (o *OpenChannelMetadataEntry) GetUpdatedAt() int64`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *OpenChannelMetadataEntry) GetUpdatedAtOk() (*int64, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *OpenChannelMetadataEntry) SetUpdatedAt(v int64)`

SetUpdatedAt sets UpdatedAt field to given value.

### HasUpdatedAt

`func (o *OpenChannelMetadataEntry) HasUpdatedAt() bool`

HasUpdatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



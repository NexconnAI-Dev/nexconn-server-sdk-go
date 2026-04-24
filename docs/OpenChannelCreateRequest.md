# OpenChannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | Legacy &#x60;chatroomId&#x60;. | 
**DestroyType** | Pointer to **int32** | &#39;0&#39; for inactive-time destroy and &#39;1&#39; for fixed-time destroy. | [optional] 
**TtlMinutes** | Pointer to **int32** | Legacy &#x60;destroyTime&#x60;. Valid range is 60 to 10080 minutes according to the PDF. | [optional] 
**ShouldFreeze** | Pointer to **bool** | Whether whole-channel freeze is enabled when the chatroom is created. | [optional] 
**AllowedSendersList** | Pointer to **[]string** | Allowed senders list applied when the chatroom is frozen. | [optional] 
**MetadataOwnerId** | Pointer to **string** | Legacy &#x60;entryOwnerId&#x60;. | [optional] 
**Metadata** | Pointer to **map[string]string** | Legacy &#x60;entryInfo&#x60;. Open-channel metadata key/value pairs. | [optional] 

## Methods

### NewOpenChannelCreateRequest

`func NewOpenChannelCreateRequest(channelId string, ) *OpenChannelCreateRequest`

NewOpenChannelCreateRequest instantiates a new OpenChannelCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOpenChannelCreateRequestWithDefaults

`func NewOpenChannelCreateRequestWithDefaults() *OpenChannelCreateRequest`

NewOpenChannelCreateRequestWithDefaults instantiates a new OpenChannelCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *OpenChannelCreateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *OpenChannelCreateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *OpenChannelCreateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetDestroyType

`func (o *OpenChannelCreateRequest) GetDestroyType() int32`

GetDestroyType returns the DestroyType field if non-nil, zero value otherwise.

### GetDestroyTypeOk

`func (o *OpenChannelCreateRequest) GetDestroyTypeOk() (*int32, bool)`

GetDestroyTypeOk returns a tuple with the DestroyType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDestroyType

`func (o *OpenChannelCreateRequest) SetDestroyType(v int32)`

SetDestroyType sets DestroyType field to given value.

### HasDestroyType

`func (o *OpenChannelCreateRequest) HasDestroyType() bool`

HasDestroyType returns a boolean if a field has been set.

### GetTtlMinutes

`func (o *OpenChannelCreateRequest) GetTtlMinutes() int32`

GetTtlMinutes returns the TtlMinutes field if non-nil, zero value otherwise.

### GetTtlMinutesOk

`func (o *OpenChannelCreateRequest) GetTtlMinutesOk() (*int32, bool)`

GetTtlMinutesOk returns a tuple with the TtlMinutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlMinutes

`func (o *OpenChannelCreateRequest) SetTtlMinutes(v int32)`

SetTtlMinutes sets TtlMinutes field to given value.

### HasTtlMinutes

`func (o *OpenChannelCreateRequest) HasTtlMinutes() bool`

HasTtlMinutes returns a boolean if a field has been set.

### GetShouldFreeze

`func (o *OpenChannelCreateRequest) GetShouldFreeze() bool`

GetShouldFreeze returns the ShouldFreeze field if non-nil, zero value otherwise.

### GetShouldFreezeOk

`func (o *OpenChannelCreateRequest) GetShouldFreezeOk() (*bool, bool)`

GetShouldFreezeOk returns a tuple with the ShouldFreeze field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetShouldFreeze

`func (o *OpenChannelCreateRequest) SetShouldFreeze(v bool)`

SetShouldFreeze sets ShouldFreeze field to given value.

### HasShouldFreeze

`func (o *OpenChannelCreateRequest) HasShouldFreeze() bool`

HasShouldFreeze returns a boolean if a field has been set.

### GetAllowedSendersList

`func (o *OpenChannelCreateRequest) GetAllowedSendersList() []string`

GetAllowedSendersList returns the AllowedSendersList field if non-nil, zero value otherwise.

### GetAllowedSendersListOk

`func (o *OpenChannelCreateRequest) GetAllowedSendersListOk() (*[]string, bool)`

GetAllowedSendersListOk returns a tuple with the AllowedSendersList field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedSendersList

`func (o *OpenChannelCreateRequest) SetAllowedSendersList(v []string)`

SetAllowedSendersList sets AllowedSendersList field to given value.

### HasAllowedSendersList

`func (o *OpenChannelCreateRequest) HasAllowedSendersList() bool`

HasAllowedSendersList returns a boolean if a field has been set.

### GetMetadataOwnerId

`func (o *OpenChannelCreateRequest) GetMetadataOwnerId() string`

GetMetadataOwnerId returns the MetadataOwnerId field if non-nil, zero value otherwise.

### GetMetadataOwnerIdOk

`func (o *OpenChannelCreateRequest) GetMetadataOwnerIdOk() (*string, bool)`

GetMetadataOwnerIdOk returns a tuple with the MetadataOwnerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadataOwnerId

`func (o *OpenChannelCreateRequest) SetMetadataOwnerId(v string)`

SetMetadataOwnerId sets MetadataOwnerId field to given value.

### HasMetadataOwnerId

`func (o *OpenChannelCreateRequest) HasMetadataOwnerId() bool`

HasMetadataOwnerId returns a boolean if a field has been set.

### GetMetadata

`func (o *OpenChannelCreateRequest) GetMetadata() map[string]string`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *OpenChannelCreateRequest) GetMetadataOk() (*map[string]string, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *OpenChannelCreateRequest) SetMetadata(v map[string]string)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *OpenChannelCreateRequest) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



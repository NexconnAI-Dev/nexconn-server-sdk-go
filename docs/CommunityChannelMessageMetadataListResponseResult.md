# CommunityChannelMessageMetadataListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Metadata** | Pointer to [**[]MessageMetadataListItem**](MessageMetadataListItem.md) | Same shape as channel-type list; array of &#x60;MetadataItem&#x60;. | [optional] 

## Methods

### NewCommunityChannelMessageMetadataListResponseResult

`func NewCommunityChannelMessageMetadataListResponseResult() *CommunityChannelMessageMetadataListResponseResult`

NewCommunityChannelMessageMetadataListResponseResult instantiates a new CommunityChannelMessageMetadataListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunityChannelMessageMetadataListResponseResultWithDefaults

`func NewCommunityChannelMessageMetadataListResponseResultWithDefaults() *CommunityChannelMessageMetadataListResponseResult`

NewCommunityChannelMessageMetadataListResponseResultWithDefaults instantiates a new CommunityChannelMessageMetadataListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMetadata

`func (o *CommunityChannelMessageMetadataListResponseResult) GetMetadata() []MessageMetadataListItem`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *CommunityChannelMessageMetadataListResponseResult) GetMetadataOk() (*[]MessageMetadataListItem, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *CommunityChannelMessageMetadataListResponseResult) SetMetadata(v []MessageMetadataListItem)`

SetMetadata sets Metadata field to given value.

### HasMetadata

`func (o *CommunityChannelMessageMetadataListResponseResult) HasMetadata() bool`

HasMetadata returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



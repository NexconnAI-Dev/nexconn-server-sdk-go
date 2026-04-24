# CommunitySubchannelListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subchannels** | Pointer to [**[]CommunitySubchannelItem**](CommunitySubchannelItem.md) | Lowercase property name from &#x60;CommunityChannelListResult&#x60; (&#x60;/v4/community-channel/subchannel/list&#x60;). | [optional] 

## Methods

### NewCommunitySubchannelListResponseResult

`func NewCommunitySubchannelListResponseResult() *CommunitySubchannelListResponseResult`

NewCommunitySubchannelListResponseResult instantiates a new CommunitySubchannelListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCommunitySubchannelListResponseResultWithDefaults

`func NewCommunitySubchannelListResponseResultWithDefaults() *CommunitySubchannelListResponseResult`

NewCommunitySubchannelListResponseResultWithDefaults instantiates a new CommunitySubchannelListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubchannels

`func (o *CommunitySubchannelListResponseResult) GetSubchannels() []CommunitySubchannelItem`

GetSubchannels returns the Subchannels field if non-nil, zero value otherwise.

### GetSubchannelsOk

`func (o *CommunitySubchannelListResponseResult) GetSubchannelsOk() (*[]CommunitySubchannelItem, bool)`

GetSubchannelsOk returns a tuple with the Subchannels field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubchannels

`func (o *CommunitySubchannelListResponseResult) SetSubchannels(v []CommunitySubchannelItem)`

SetSubchannels sets Subchannels field to given value.

### HasSubchannels

`func (o *CommunitySubchannelListResponseResult) HasSubchannels() bool`

HasSubchannels returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# GroupChannelListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** |  | [optional] 
**Groups** | Pointer to [**[]GroupChannelSummaryItem**](GroupChannelSummaryItem.md) |  | [optional] 

## Methods

### NewGroupChannelListResponseResult

`func NewGroupChannelListResponseResult() *GroupChannelListResponseResult`

NewGroupChannelListResponseResult instantiates a new GroupChannelListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelListResponseResultWithDefaults

`func NewGroupChannelListResponseResultWithDefaults() *GroupChannelListResponseResult`

NewGroupChannelListResponseResultWithDefaults instantiates a new GroupChannelListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *GroupChannelListResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelListResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelListResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelListResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetGroups

`func (o *GroupChannelListResponseResult) GetGroups() []GroupChannelSummaryItem`

GetGroups returns the Groups field if non-nil, zero value otherwise.

### GetGroupsOk

`func (o *GroupChannelListResponseResult) GetGroupsOk() (*[]GroupChannelSummaryItem, bool)`

GetGroupsOk returns a tuple with the Groups field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroups

`func (o *GroupChannelListResponseResult) SetGroups(v []GroupChannelSummaryItem)`

SetGroups sets Groups field to given value.

### HasGroups

`func (o *GroupChannelListResponseResult) HasGroups() bool`

HasGroups returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



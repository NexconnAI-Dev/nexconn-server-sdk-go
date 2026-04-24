# GroupChannelJoinedListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** |  | [optional] 
**Groups** | Pointer to [**[]GroupChannelJoinedItem**](GroupChannelJoinedItem.md) |  | [optional] 

## Methods

### NewGroupChannelJoinedListResponseResult

`func NewGroupChannelJoinedListResponseResult() *GroupChannelJoinedListResponseResult`

NewGroupChannelJoinedListResponseResult instantiates a new GroupChannelJoinedListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelJoinedListResponseResultWithDefaults

`func NewGroupChannelJoinedListResponseResultWithDefaults() *GroupChannelJoinedListResponseResult`

NewGroupChannelJoinedListResponseResultWithDefaults instantiates a new GroupChannelJoinedListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *GroupChannelJoinedListResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelJoinedListResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelJoinedListResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelJoinedListResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetGroups

`func (o *GroupChannelJoinedListResponseResult) GetGroups() []GroupChannelJoinedItem`

GetGroups returns the Groups field if non-nil, zero value otherwise.

### GetGroupsOk

`func (o *GroupChannelJoinedListResponseResult) GetGroupsOk() (*[]GroupChannelJoinedItem, bool)`

GetGroupsOk returns a tuple with the Groups field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroups

`func (o *GroupChannelJoinedListResponseResult) SetGroups(v []GroupChannelJoinedItem)`

SetGroups sets Groups field to given value.

### HasGroups

`func (o *GroupChannelJoinedListResponseResult) HasGroups() bool`

HasGroups returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



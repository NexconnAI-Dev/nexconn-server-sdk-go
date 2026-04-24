# GroupChannelMemberBatchGetResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** | From &#x60;EGMemberListResult.pageToken&#x60;. | [optional] 
**TotalCount** | Pointer to **int32** | From &#x60;EGMemberListResult.totalCount&#x60;. | [optional] 
**Members** | Pointer to [**[]GroupChannelMemberItem**](GroupChannelMemberItem.md) |  | [optional] 

## Methods

### NewGroupChannelMemberBatchGetResponseResult

`func NewGroupChannelMemberBatchGetResponseResult() *GroupChannelMemberBatchGetResponseResult`

NewGroupChannelMemberBatchGetResponseResult instantiates a new GroupChannelMemberBatchGetResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberBatchGetResponseResultWithDefaults

`func NewGroupChannelMemberBatchGetResponseResultWithDefaults() *GroupChannelMemberBatchGetResponseResult`

NewGroupChannelMemberBatchGetResponseResultWithDefaults instantiates a new GroupChannelMemberBatchGetResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *GroupChannelMemberBatchGetResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelMemberBatchGetResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelMemberBatchGetResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelMemberBatchGetResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetTotalCount

`func (o *GroupChannelMemberBatchGetResponseResult) GetTotalCount() int32`

GetTotalCount returns the TotalCount field if non-nil, zero value otherwise.

### GetTotalCountOk

`func (o *GroupChannelMemberBatchGetResponseResult) GetTotalCountOk() (*int32, bool)`

GetTotalCountOk returns a tuple with the TotalCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotalCount

`func (o *GroupChannelMemberBatchGetResponseResult) SetTotalCount(v int32)`

SetTotalCount sets TotalCount field to given value.

### HasTotalCount

`func (o *GroupChannelMemberBatchGetResponseResult) HasTotalCount() bool`

HasTotalCount returns a boolean if a field has been set.

### GetMembers

`func (o *GroupChannelMemberBatchGetResponseResult) GetMembers() []GroupChannelMemberItem`

GetMembers returns the Members field if non-nil, zero value otherwise.

### GetMembersOk

`func (o *GroupChannelMemberBatchGetResponseResult) GetMembersOk() (*[]GroupChannelMemberItem, bool)`

GetMembersOk returns a tuple with the Members field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMembers

`func (o *GroupChannelMemberBatchGetResponseResult) SetMembers(v []GroupChannelMemberItem)`

SetMembers sets Members field to given value.

### HasMembers

`func (o *GroupChannelMemberBatchGetResponseResult) HasMembers() bool`

HasMembers returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



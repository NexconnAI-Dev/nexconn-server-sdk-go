# GroupChannelMemberListResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TotalCount** | Pointer to **int32** |  | [optional] 
**PageToken** | Pointer to **string** |  | [optional] 
**Members** | Pointer to [**[]GroupChannelMemberItem**](GroupChannelMemberItem.md) |  | [optional] 

## Methods

### NewGroupChannelMemberListResponseResult

`func NewGroupChannelMemberListResponseResult() *GroupChannelMemberListResponseResult`

NewGroupChannelMemberListResponseResult instantiates a new GroupChannelMemberListResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelMemberListResponseResultWithDefaults

`func NewGroupChannelMemberListResponseResultWithDefaults() *GroupChannelMemberListResponseResult`

NewGroupChannelMemberListResponseResultWithDefaults instantiates a new GroupChannelMemberListResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTotalCount

`func (o *GroupChannelMemberListResponseResult) GetTotalCount() int32`

GetTotalCount returns the TotalCount field if non-nil, zero value otherwise.

### GetTotalCountOk

`func (o *GroupChannelMemberListResponseResult) GetTotalCountOk() (*int32, bool)`

GetTotalCountOk returns a tuple with the TotalCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotalCount

`func (o *GroupChannelMemberListResponseResult) SetTotalCount(v int32)`

SetTotalCount sets TotalCount field to given value.

### HasTotalCount

`func (o *GroupChannelMemberListResponseResult) HasTotalCount() bool`

HasTotalCount returns a boolean if a field has been set.

### GetPageToken

`func (o *GroupChannelMemberListResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *GroupChannelMemberListResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *GroupChannelMemberListResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *GroupChannelMemberListResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetMembers

`func (o *GroupChannelMemberListResponseResult) GetMembers() []GroupChannelMemberItem`

GetMembers returns the Members field if non-nil, zero value otherwise.

### GetMembersOk

`func (o *GroupChannelMemberListResponseResult) GetMembersOk() (*[]GroupChannelMemberItem, bool)`

GetMembersOk returns a tuple with the Members field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMembers

`func (o *GroupChannelMemberListResponseResult) SetMembers(v []GroupChannelMemberItem)`

SetMembers sets Members field to given value.

### HasMembers

`func (o *GroupChannelMemberListResponseResult) HasMembers() bool`

HasMembers returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



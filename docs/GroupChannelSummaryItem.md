# GroupChannelSummaryItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | Pointer to **string** |  | [optional] 
**Name** | Pointer to **string** |  | [optional] 
**GroupProfile** | Pointer to **map[string]interface{}** | Group basic profile object as in &#x60;EGGroupListResult.GroupItem.groupProfile&#x60;. | [optional] 
**Creator** | Pointer to **string** | Group creator user ID. | [optional] 
**Owner** | Pointer to **string** |  | [optional] 
**CreatedAt** | Pointer to **int64** |  | [optional] 

## Methods

### NewGroupChannelSummaryItem

`func NewGroupChannelSummaryItem() *GroupChannelSummaryItem`

NewGroupChannelSummaryItem instantiates a new GroupChannelSummaryItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelSummaryItemWithDefaults

`func NewGroupChannelSummaryItemWithDefaults() *GroupChannelSummaryItem`

NewGroupChannelSummaryItemWithDefaults instantiates a new GroupChannelSummaryItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelSummaryItem) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelSummaryItem) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelSummaryItem) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.

### HasChannelId

`func (o *GroupChannelSummaryItem) HasChannelId() bool`

HasChannelId returns a boolean if a field has been set.

### GetName

`func (o *GroupChannelSummaryItem) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *GroupChannelSummaryItem) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *GroupChannelSummaryItem) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *GroupChannelSummaryItem) HasName() bool`

HasName returns a boolean if a field has been set.

### GetGroupProfile

`func (o *GroupChannelSummaryItem) GetGroupProfile() map[string]interface{}`

GetGroupProfile returns the GroupProfile field if non-nil, zero value otherwise.

### GetGroupProfileOk

`func (o *GroupChannelSummaryItem) GetGroupProfileOk() (*map[string]interface{}, bool)`

GetGroupProfileOk returns a tuple with the GroupProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupProfile

`func (o *GroupChannelSummaryItem) SetGroupProfile(v map[string]interface{})`

SetGroupProfile sets GroupProfile field to given value.

### HasGroupProfile

`func (o *GroupChannelSummaryItem) HasGroupProfile() bool`

HasGroupProfile returns a boolean if a field has been set.

### GetCreator

`func (o *GroupChannelSummaryItem) GetCreator() string`

GetCreator returns the Creator field if non-nil, zero value otherwise.

### GetCreatorOk

`func (o *GroupChannelSummaryItem) GetCreatorOk() (*string, bool)`

GetCreatorOk returns a tuple with the Creator field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreator

`func (o *GroupChannelSummaryItem) SetCreator(v string)`

SetCreator sets Creator field to given value.

### HasCreator

`func (o *GroupChannelSummaryItem) HasCreator() bool`

HasCreator returns a boolean if a field has been set.

### GetOwner

`func (o *GroupChannelSummaryItem) GetOwner() string`

GetOwner returns the Owner field if non-nil, zero value otherwise.

### GetOwnerOk

`func (o *GroupChannelSummaryItem) GetOwnerOk() (*string, bool)`

GetOwnerOk returns a tuple with the Owner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOwner

`func (o *GroupChannelSummaryItem) SetOwner(v string)`

SetOwner sets Owner field to given value.

### HasOwner

`func (o *GroupChannelSummaryItem) HasOwner() bool`

HasOwner returns a boolean if a field has been set.

### GetCreatedAt

`func (o *GroupChannelSummaryItem) GetCreatedAt() int64`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *GroupChannelSummaryItem) GetCreatedAtOk() (*int64, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *GroupChannelSummaryItem) SetCreatedAt(v int64)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *GroupChannelSummaryItem) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



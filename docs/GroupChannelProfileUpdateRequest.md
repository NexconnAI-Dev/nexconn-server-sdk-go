# GroupChannelProfileUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | Legacy &#x60;groupId&#x60;. | 
**GroupProfile** | Pointer to **map[string]interface{}** | Group basic profile object defined by the source API. | [optional] 
**Permissions** | Pointer to **map[string]interface{}** | Group permission object defined by the source API. | [optional] 
**GroupExtProfile** | Pointer to **map[string]string** | Group extra profile object. Keys should use the &#x60;ext_&#x60; prefix and support up to 10 entries. | [optional] 

## Methods

### NewGroupChannelProfileUpdateRequest

`func NewGroupChannelProfileUpdateRequest(channelId string, ) *GroupChannelProfileUpdateRequest`

NewGroupChannelProfileUpdateRequest instantiates a new GroupChannelProfileUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelProfileUpdateRequestWithDefaults

`func NewGroupChannelProfileUpdateRequestWithDefaults() *GroupChannelProfileUpdateRequest`

NewGroupChannelProfileUpdateRequestWithDefaults instantiates a new GroupChannelProfileUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelProfileUpdateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelProfileUpdateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelProfileUpdateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetGroupProfile

`func (o *GroupChannelProfileUpdateRequest) GetGroupProfile() map[string]interface{}`

GetGroupProfile returns the GroupProfile field if non-nil, zero value otherwise.

### GetGroupProfileOk

`func (o *GroupChannelProfileUpdateRequest) GetGroupProfileOk() (*map[string]interface{}, bool)`

GetGroupProfileOk returns a tuple with the GroupProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupProfile

`func (o *GroupChannelProfileUpdateRequest) SetGroupProfile(v map[string]interface{})`

SetGroupProfile sets GroupProfile field to given value.

### HasGroupProfile

`func (o *GroupChannelProfileUpdateRequest) HasGroupProfile() bool`

HasGroupProfile returns a boolean if a field has been set.

### GetPermissions

`func (o *GroupChannelProfileUpdateRequest) GetPermissions() map[string]interface{}`

GetPermissions returns the Permissions field if non-nil, zero value otherwise.

### GetPermissionsOk

`func (o *GroupChannelProfileUpdateRequest) GetPermissionsOk() (*map[string]interface{}, bool)`

GetPermissionsOk returns a tuple with the Permissions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissions

`func (o *GroupChannelProfileUpdateRequest) SetPermissions(v map[string]interface{})`

SetPermissions sets Permissions field to given value.

### HasPermissions

`func (o *GroupChannelProfileUpdateRequest) HasPermissions() bool`

HasPermissions returns a boolean if a field has been set.

### GetGroupExtProfile

`func (o *GroupChannelProfileUpdateRequest) GetGroupExtProfile() map[string]string`

GetGroupExtProfile returns the GroupExtProfile field if non-nil, zero value otherwise.

### GetGroupExtProfileOk

`func (o *GroupChannelProfileUpdateRequest) GetGroupExtProfileOk() (*map[string]string, bool)`

GetGroupExtProfileOk returns a tuple with the GroupExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupExtProfile

`func (o *GroupChannelProfileUpdateRequest) SetGroupExtProfile(v map[string]string)`

SetGroupExtProfile sets GroupExtProfile field to given value.

### HasGroupExtProfile

`func (o *GroupChannelProfileUpdateRequest) HasGroupExtProfile() bool`

HasGroupExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# GroupChannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | Legacy &#x60;groupId&#x60;. | 
**Name** | **string** |  | 
**Owner** | **string** | Group owner user ID. | 
**UserIds** | Pointer to **[]string** | Invited user IDs. The PDF limits this array to 30 users per request. | [optional] 
**GroupProfile** | Pointer to **map[string]interface{}** | Group basic profile object. Common keys include &#x60;introduction&#x60;, &#x60;announcement&#x60;, and &#x60;portraitUrl&#x60;. | [optional] 
**Permissions** | Pointer to **map[string]interface{}** | Group permission object defined by the source API. | [optional] 
**GroupExtProfile** | Pointer to **map[string]interface{}** | Group extra profile object. Keys must start with &#x60;ext_&#x60; according to the PDF. | [optional] 

## Methods

### NewGroupChannelCreateRequest

`func NewGroupChannelCreateRequest(channelId string, name string, owner string, ) *GroupChannelCreateRequest`

NewGroupChannelCreateRequest instantiates a new GroupChannelCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupChannelCreateRequestWithDefaults

`func NewGroupChannelCreateRequestWithDefaults() *GroupChannelCreateRequest`

NewGroupChannelCreateRequestWithDefaults instantiates a new GroupChannelCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetChannelId

`func (o *GroupChannelCreateRequest) GetChannelId() string`

GetChannelId returns the ChannelId field if non-nil, zero value otherwise.

### GetChannelIdOk

`func (o *GroupChannelCreateRequest) GetChannelIdOk() (*string, bool)`

GetChannelIdOk returns a tuple with the ChannelId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChannelId

`func (o *GroupChannelCreateRequest) SetChannelId(v string)`

SetChannelId sets ChannelId field to given value.


### GetName

`func (o *GroupChannelCreateRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *GroupChannelCreateRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *GroupChannelCreateRequest) SetName(v string)`

SetName sets Name field to given value.


### GetOwner

`func (o *GroupChannelCreateRequest) GetOwner() string`

GetOwner returns the Owner field if non-nil, zero value otherwise.

### GetOwnerOk

`func (o *GroupChannelCreateRequest) GetOwnerOk() (*string, bool)`

GetOwnerOk returns a tuple with the Owner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOwner

`func (o *GroupChannelCreateRequest) SetOwner(v string)`

SetOwner sets Owner field to given value.


### GetUserIds

`func (o *GroupChannelCreateRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *GroupChannelCreateRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *GroupChannelCreateRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.

### HasUserIds

`func (o *GroupChannelCreateRequest) HasUserIds() bool`

HasUserIds returns a boolean if a field has been set.

### GetGroupProfile

`func (o *GroupChannelCreateRequest) GetGroupProfile() map[string]interface{}`

GetGroupProfile returns the GroupProfile field if non-nil, zero value otherwise.

### GetGroupProfileOk

`func (o *GroupChannelCreateRequest) GetGroupProfileOk() (*map[string]interface{}, bool)`

GetGroupProfileOk returns a tuple with the GroupProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupProfile

`func (o *GroupChannelCreateRequest) SetGroupProfile(v map[string]interface{})`

SetGroupProfile sets GroupProfile field to given value.

### HasGroupProfile

`func (o *GroupChannelCreateRequest) HasGroupProfile() bool`

HasGroupProfile returns a boolean if a field has been set.

### GetPermissions

`func (o *GroupChannelCreateRequest) GetPermissions() map[string]interface{}`

GetPermissions returns the Permissions field if non-nil, zero value otherwise.

### GetPermissionsOk

`func (o *GroupChannelCreateRequest) GetPermissionsOk() (*map[string]interface{}, bool)`

GetPermissionsOk returns a tuple with the Permissions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPermissions

`func (o *GroupChannelCreateRequest) SetPermissions(v map[string]interface{})`

SetPermissions sets Permissions field to given value.

### HasPermissions

`func (o *GroupChannelCreateRequest) HasPermissions() bool`

HasPermissions returns a boolean if a field has been set.

### GetGroupExtProfile

`func (o *GroupChannelCreateRequest) GetGroupExtProfile() map[string]interface{}`

GetGroupExtProfile returns the GroupExtProfile field if non-nil, zero value otherwise.

### GetGroupExtProfileOk

`func (o *GroupChannelCreateRequest) GetGroupExtProfileOk() (*map[string]interface{}, bool)`

GetGroupExtProfileOk returns a tuple with the GroupExtProfile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupExtProfile

`func (o *GroupChannelCreateRequest) SetGroupExtProfile(v map[string]interface{})`

SetGroupExtProfile sets GroupExtProfile field to given value.

### HasGroupExtProfile

`func (o *GroupChannelCreateRequest) HasGroupExtProfile() bool`

HasGroupExtProfile returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



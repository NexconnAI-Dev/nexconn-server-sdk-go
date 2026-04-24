# UserTagBatchSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserIds** | **[]string** |  | 
**Tags** | **[]string** | Full replacement set of user tags. Sending an empty array clears all tags. | 

## Methods

### NewUserTagBatchSetRequest

`func NewUserTagBatchSetRequest(userIds []string, tags []string, ) *UserTagBatchSetRequest`

NewUserTagBatchSetRequest instantiates a new UserTagBatchSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserTagBatchSetRequestWithDefaults

`func NewUserTagBatchSetRequestWithDefaults() *UserTagBatchSetRequest`

NewUserTagBatchSetRequestWithDefaults instantiates a new UserTagBatchSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserIds

`func (o *UserTagBatchSetRequest) GetUserIds() []string`

GetUserIds returns the UserIds field if non-nil, zero value otherwise.

### GetUserIdsOk

`func (o *UserTagBatchSetRequest) GetUserIdsOk() (*[]string, bool)`

GetUserIdsOk returns a tuple with the UserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserIds

`func (o *UserTagBatchSetRequest) SetUserIds(v []string)`

SetUserIds sets UserIds field to given value.


### GetTags

`func (o *UserTagBatchSetRequest) GetTags() []string`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *UserTagBatchSetRequest) GetTagsOk() (*[]string, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *UserTagBatchSetRequest) SetTags(v []string)`

SetTags sets Tags field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# UserChannelTagRemoveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**TagIds** | **[]string** |  | 

## Methods

### NewUserChannelTagRemoveRequest

`func NewUserChannelTagRemoveRequest(userId string, tagIds []string, ) *UserChannelTagRemoveRequest`

NewUserChannelTagRemoveRequest instantiates a new UserChannelTagRemoveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserChannelTagRemoveRequestWithDefaults

`func NewUserChannelTagRemoveRequestWithDefaults() *UserChannelTagRemoveRequest`

NewUserChannelTagRemoveRequestWithDefaults instantiates a new UserChannelTagRemoveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserChannelTagRemoveRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserChannelTagRemoveRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserChannelTagRemoveRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetTagIds

`func (o *UserChannelTagRemoveRequest) GetTagIds() []string`

GetTagIds returns the TagIds field if non-nil, zero value otherwise.

### GetTagIdsOk

`func (o *UserChannelTagRemoveRequest) GetTagIdsOk() (*[]string, bool)`

GetTagIdsOk returns a tuple with the TagIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTagIds

`func (o *UserChannelTagRemoveRequest) SetTagIds(v []string)`

SetTagIds sets TagIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AccessTokenIssueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**Name** | **string** |  | 
**AvatarUrl** | Pointer to **string** |  | [optional] 

## Methods

### NewAccessTokenIssueRequest

`func NewAccessTokenIssueRequest(userId string, name string, ) *AccessTokenIssueRequest`

NewAccessTokenIssueRequest instantiates a new AccessTokenIssueRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAccessTokenIssueRequestWithDefaults

`func NewAccessTokenIssueRequestWithDefaults() *AccessTokenIssueRequest`

NewAccessTokenIssueRequestWithDefaults instantiates a new AccessTokenIssueRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *AccessTokenIssueRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *AccessTokenIssueRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *AccessTokenIssueRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetName

`func (o *AccessTokenIssueRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *AccessTokenIssueRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *AccessTokenIssueRequest) SetName(v string)`

SetName sets Name field to given value.


### GetAvatarUrl

`func (o *AccessTokenIssueRequest) GetAvatarUrl() string`

GetAvatarUrl returns the AvatarUrl field if non-nil, zero value otherwise.

### GetAvatarUrlOk

`func (o *AccessTokenIssueRequest) GetAvatarUrlOk() (*string, bool)`

GetAvatarUrlOk returns a tuple with the AvatarUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAvatarUrl

`func (o *AccessTokenIssueRequest) SetAvatarUrl(v string)`

SetAvatarUrl sets AvatarUrl field to given value.

### HasAvatarUrl

`func (o *AccessTokenIssueRequest) HasAvatarUrl() bool`

HasAvatarUrl returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



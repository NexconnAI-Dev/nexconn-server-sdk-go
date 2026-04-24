# AccessTokenIssueResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | Pointer to **string** | User ID that the issued access token belongs to. | [optional] 
**AccessToken** | Pointer to **string** | Issued access token for subsequent user-authenticated requests. | [optional] 

## Methods

### NewAccessTokenIssueResult

`func NewAccessTokenIssueResult() *AccessTokenIssueResult`

NewAccessTokenIssueResult instantiates a new AccessTokenIssueResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAccessTokenIssueResultWithDefaults

`func NewAccessTokenIssueResultWithDefaults() *AccessTokenIssueResult`

NewAccessTokenIssueResultWithDefaults instantiates a new AccessTokenIssueResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *AccessTokenIssueResult) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *AccessTokenIssueResult) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *AccessTokenIssueResult) SetUserId(v string)`

SetUserId sets UserId field to given value.

### HasUserId

`func (o *AccessTokenIssueResult) HasUserId() bool`

HasUserId returns a boolean if a field has been set.

### GetAccessToken

`func (o *AccessTokenIssueResult) GetAccessToken() string`

GetAccessToken returns the AccessToken field if non-nil, zero value otherwise.

### GetAccessTokenOk

`func (o *AccessTokenIssueResult) GetAccessTokenOk() (*string, bool)`

GetAccessTokenOk returns a tuple with the AccessToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAccessToken

`func (o *AccessTokenIssueResult) SetAccessToken(v string)`

SetAccessToken sets AccessToken field to given value.

### HasAccessToken

`func (o *AccessTokenIssueResult) HasAccessToken() bool`

HasAccessToken returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



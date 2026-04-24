# UserProfileSetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int32** |  | 
**ProfileKey** | Pointer to **string** | Returns the failed profile key when the update fails. | [optional] 

## Methods

### NewUserProfileSetResponse

`func NewUserProfileSetResponse(code int32, ) *UserProfileSetResponse`

NewUserProfileSetResponse instantiates a new UserProfileSetResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserProfileSetResponseWithDefaults

`func NewUserProfileSetResponseWithDefaults() *UserProfileSetResponse`

NewUserProfileSetResponseWithDefaults instantiates a new UserProfileSetResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCode

`func (o *UserProfileSetResponse) GetCode() int32`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *UserProfileSetResponse) GetCodeOk() (*int32, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *UserProfileSetResponse) SetCode(v int32)`

SetCode sets Code field to given value.


### GetProfileKey

`func (o *UserProfileSetResponse) GetProfileKey() string`

GetProfileKey returns the ProfileKey field if non-nil, zero value otherwise.

### GetProfileKeyOk

`func (o *UserProfileSetResponse) GetProfileKeyOk() (*string, bool)`

GetProfileKeyOk returns a tuple with the ProfileKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProfileKey

`func (o *UserProfileSetResponse) SetProfileKey(v string)`

SetProfileKey sets ProfileKey field to given value.

### HasProfileKey

`func (o *UserProfileSetResponse) HasProfileKey() bool`

HasProfileKey returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



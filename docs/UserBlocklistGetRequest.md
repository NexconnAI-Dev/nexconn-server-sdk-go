# UserBlocklistGetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** |  | 
**PageToken** | Pointer to **string** |  | [optional] 
**PageSize** | Pointer to **int32** |  | [optional] [default to 1000]
**Order** | Pointer to **int32** | From &#x60;PageableInput.order&#x60;. | [optional] [default to 0]

## Methods

### NewUserBlocklistGetRequest

`func NewUserBlocklistGetRequest(userId string, ) *UserBlocklistGetRequest`

NewUserBlocklistGetRequest instantiates a new UserBlocklistGetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBlocklistGetRequestWithDefaults

`func NewUserBlocklistGetRequestWithDefaults() *UserBlocklistGetRequest`

NewUserBlocklistGetRequestWithDefaults instantiates a new UserBlocklistGetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserId

`func (o *UserBlocklistGetRequest) GetUserId() string`

GetUserId returns the UserId field if non-nil, zero value otherwise.

### GetUserIdOk

`func (o *UserBlocklistGetRequest) GetUserIdOk() (*string, bool)`

GetUserIdOk returns a tuple with the UserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserId

`func (o *UserBlocklistGetRequest) SetUserId(v string)`

SetUserId sets UserId field to given value.


### GetPageToken

`func (o *UserBlocklistGetRequest) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *UserBlocklistGetRequest) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *UserBlocklistGetRequest) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *UserBlocklistGetRequest) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetPageSize

`func (o *UserBlocklistGetRequest) GetPageSize() int32`

GetPageSize returns the PageSize field if non-nil, zero value otherwise.

### GetPageSizeOk

`func (o *UserBlocklistGetRequest) GetPageSizeOk() (*int32, bool)`

GetPageSizeOk returns a tuple with the PageSize field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageSize

`func (o *UserBlocklistGetRequest) SetPageSize(v int32)`

SetPageSize sets PageSize field to given value.

### HasPageSize

`func (o *UserBlocklistGetRequest) HasPageSize() bool`

HasPageSize returns a boolean if a field has been set.

### GetOrder

`func (o *UserBlocklistGetRequest) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *UserBlocklistGetRequest) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *UserBlocklistGetRequest) SetOrder(v int32)`

SetOrder sets Order field to given value.

### HasOrder

`func (o *UserBlocklistGetRequest) HasOrder() bool`

HasOrder returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



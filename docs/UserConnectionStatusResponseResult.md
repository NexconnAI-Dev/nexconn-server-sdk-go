# UserConnectionStatusResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | Pointer to **string** | &#x60;1&#x60; means online and &#x60;0&#x60; means offline. | [optional] 

## Methods

### NewUserConnectionStatusResponseResult

`func NewUserConnectionStatusResponseResult() *UserConnectionStatusResponseResult`

NewUserConnectionStatusResponseResult instantiates a new UserConnectionStatusResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserConnectionStatusResponseResultWithDefaults

`func NewUserConnectionStatusResponseResultWithDefaults() *UserConnectionStatusResponseResult`

NewUserConnectionStatusResponseResultWithDefaults instantiates a new UserConnectionStatusResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatus

`func (o *UserConnectionStatusResponseResult) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *UserConnectionStatusResponseResult) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *UserConnectionStatusResponseResult) SetStatus(v string)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *UserConnectionStatusResponseResult) HasStatus() bool`

HasStatus returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



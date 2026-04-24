# ProfanityWordListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FilterType** | Pointer to **string** | Legacy &#x60;type&#x60;. &#x60;0&#x60; for replacement words, &#x60;1&#x60; for blocked words, and &#x60;2&#x60; for all words. PDF documents this field as a string. | [optional] [default to "1"]

## Methods

### NewProfanityWordListRequest

`func NewProfanityWordListRequest() *ProfanityWordListRequest`

NewProfanityWordListRequest instantiates a new ProfanityWordListRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProfanityWordListRequestWithDefaults

`func NewProfanityWordListRequestWithDefaults() *ProfanityWordListRequest`

NewProfanityWordListRequestWithDefaults instantiates a new ProfanityWordListRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFilterType

`func (o *ProfanityWordListRequest) GetFilterType() string`

GetFilterType returns the FilterType field if non-nil, zero value otherwise.

### GetFilterTypeOk

`func (o *ProfanityWordListRequest) GetFilterTypeOk() (*string, bool)`

GetFilterTypeOk returns a tuple with the FilterType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFilterType

`func (o *ProfanityWordListRequest) SetFilterType(v string)`

SetFilterType sets FilterType field to given value.

### HasFilterType

`func (o *ProfanityWordListRequest) HasFilterType() bool`

HasFilterType returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



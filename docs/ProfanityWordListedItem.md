# ProfanityWordListedItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Word** | Pointer to **string** | Profanity word content. | [optional] 
**Replacement** | Pointer to **string** | Replacement content. Empty means the word is blocked. | [optional] 
**FilterType** | Pointer to **string** | Result type. &#x60;0&#x60; means replacement word and &#x60;1&#x60; means blocked word. | [optional] 

## Methods

### NewProfanityWordListedItem

`func NewProfanityWordListedItem() *ProfanityWordListedItem`

NewProfanityWordListedItem instantiates a new ProfanityWordListedItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProfanityWordListedItemWithDefaults

`func NewProfanityWordListedItemWithDefaults() *ProfanityWordListedItem`

NewProfanityWordListedItemWithDefaults instantiates a new ProfanityWordListedItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetWord

`func (o *ProfanityWordListedItem) GetWord() string`

GetWord returns the Word field if non-nil, zero value otherwise.

### GetWordOk

`func (o *ProfanityWordListedItem) GetWordOk() (*string, bool)`

GetWordOk returns a tuple with the Word field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWord

`func (o *ProfanityWordListedItem) SetWord(v string)`

SetWord sets Word field to given value.

### HasWord

`func (o *ProfanityWordListedItem) HasWord() bool`

HasWord returns a boolean if a field has been set.

### GetReplacement

`func (o *ProfanityWordListedItem) GetReplacement() string`

GetReplacement returns the Replacement field if non-nil, zero value otherwise.

### GetReplacementOk

`func (o *ProfanityWordListedItem) GetReplacementOk() (*string, bool)`

GetReplacementOk returns a tuple with the Replacement field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReplacement

`func (o *ProfanityWordListedItem) SetReplacement(v string)`

SetReplacement sets Replacement field to given value.

### HasReplacement

`func (o *ProfanityWordListedItem) HasReplacement() bool`

HasReplacement returns a boolean if a field has been set.

### GetFilterType

`func (o *ProfanityWordListedItem) GetFilterType() string`

GetFilterType returns the FilterType field if non-nil, zero value otherwise.

### GetFilterTypeOk

`func (o *ProfanityWordListedItem) GetFilterTypeOk() (*string, bool)`

GetFilterTypeOk returns a tuple with the FilterType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFilterType

`func (o *ProfanityWordListedItem) SetFilterType(v string)`

SetFilterType sets FilterType field to given value.

### HasFilterType

`func (o *ProfanityWordListedItem) HasFilterType() bool`

HasFilterType returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



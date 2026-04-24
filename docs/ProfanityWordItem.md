# ProfanityWordItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Word** | **string** | Profanity word content. | 
**Replacement** | Pointer to **string** | Replacement content. When omitted, messages containing the word are blocked instead of replaced. | [optional] 

## Methods

### NewProfanityWordItem

`func NewProfanityWordItem(word string, ) *ProfanityWordItem`

NewProfanityWordItem instantiates a new ProfanityWordItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProfanityWordItemWithDefaults

`func NewProfanityWordItemWithDefaults() *ProfanityWordItem`

NewProfanityWordItemWithDefaults instantiates a new ProfanityWordItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetWord

`func (o *ProfanityWordItem) GetWord() string`

GetWord returns the Word field if non-nil, zero value otherwise.

### GetWordOk

`func (o *ProfanityWordItem) GetWordOk() (*string, bool)`

GetWordOk returns a tuple with the Word field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWord

`func (o *ProfanityWordItem) SetWord(v string)`

SetWord sets Word field to given value.


### GetReplacement

`func (o *ProfanityWordItem) GetReplacement() string`

GetReplacement returns the Replacement field if non-nil, zero value otherwise.

### GetReplacementOk

`func (o *ProfanityWordItem) GetReplacementOk() (*string, bool)`

GetReplacementOk returns a tuple with the Replacement field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReplacement

`func (o *ProfanityWordItem) SetReplacement(v string)`

SetReplacement sets Replacement field to given value.

### HasReplacement

`func (o *ProfanityWordItem) HasReplacement() bool`

HasReplacement returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



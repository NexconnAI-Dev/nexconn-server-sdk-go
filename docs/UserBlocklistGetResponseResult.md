# UserBlocklistGetResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageToken** | Pointer to **string** | Next page cursor; matches &#x60;BlocklistListResult.pageToken&#x60; (not &#x60;next&#x60;). | [optional] 
**BlockedUserIds** | Pointer to **[]string** |  | [optional] 

## Methods

### NewUserBlocklistGetResponseResult

`func NewUserBlocklistGetResponseResult() *UserBlocklistGetResponseResult`

NewUserBlocklistGetResponseResult instantiates a new UserBlocklistGetResponseResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewUserBlocklistGetResponseResultWithDefaults

`func NewUserBlocklistGetResponseResultWithDefaults() *UserBlocklistGetResponseResult`

NewUserBlocklistGetResponseResultWithDefaults instantiates a new UserBlocklistGetResponseResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageToken

`func (o *UserBlocklistGetResponseResult) GetPageToken() string`

GetPageToken returns the PageToken field if non-nil, zero value otherwise.

### GetPageTokenOk

`func (o *UserBlocklistGetResponseResult) GetPageTokenOk() (*string, bool)`

GetPageTokenOk returns a tuple with the PageToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageToken

`func (o *UserBlocklistGetResponseResult) SetPageToken(v string)`

SetPageToken sets PageToken field to given value.

### HasPageToken

`func (o *UserBlocklistGetResponseResult) HasPageToken() bool`

HasPageToken returns a boolean if a field has been set.

### GetBlockedUserIds

`func (o *UserBlocklistGetResponseResult) GetBlockedUserIds() []string`

GetBlockedUserIds returns the BlockedUserIds field if non-nil, zero value otherwise.

### GetBlockedUserIdsOk

`func (o *UserBlocklistGetResponseResult) GetBlockedUserIdsOk() (*[]string, bool)`

GetBlockedUserIdsOk returns a tuple with the BlockedUserIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBlockedUserIds

`func (o *UserBlocklistGetResponseResult) SetBlockedUserIds(v []string)`

SetBlockedUserIds sets BlockedUserIds field to given value.

### HasBlockedUserIds

`func (o *UserBlocklistGetResponseResult) HasBlockedUserIds() bool`

HasBlockedUserIds returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



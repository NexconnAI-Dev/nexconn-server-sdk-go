# nexconn-server-sdk-go

OpenAPI specification aligned with the current Nexconn public documentation, PDF source documents, and generated SDK requirements.

## Overview

- API version: 0.1.1
- Package version: 0.1.1
- Generator version: 7.14.0
- Build package: org.openapitools.codegen.languages.GoClientCodegen

## Installation

The module is hosted on **GitHub** at `https://github.com/NexconnAI-Dev/nexconn-server-sdk-go`.

From your module root (next to `go.mod`), add the dependency:

```sh
go get github.com/NexconnAI-Dev/nexconn-server-sdk-go@latest
```

Or add a `require github.com/NexconnAI-Dev/nexconn-server-sdk-go v…` line to `go.mod` and run `go mod tidy`. Prefer a **release tag** instead of `@latest` when tags exist (for example `go get github.com/NexconnAI-Dev/nexconn-server-sdk-go@v0.1.0`).

Import:

```go
import ncsdk "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
```

## Quick Start

The example below uses the SDK's built-in signing support to inject `App-Key / Nonce / Timestamp / Signature / X-Request-ID` automatically.

```go
package main

import (
	"context"
	"fmt"
	"log"
	"os"

	ncsdk "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

func main() {
	cfg := ncsdk.NewConfiguration()
	cfg.SetNexconnCredentials(
		os.Getenv("NEXCONN_APP_KEY"),
		os.Getenv("NEXCONN_APP_SECRET"),
	)
	if err := cfg.SetPrimaryBackupDomains(
		os.Getenv("NEXCONN_PRIMARY_API_DOMAIN"),
		os.Getenv("NEXCONN_SECONDARY_API_DOMAIN"),
	); err != nil {
		log.Fatalf("configure domains failed: %v", err)
	}

	// Optional: override the default nonce generator
	// cfg.SetNonceGenerator(func() string { return "custom-nonce" })

	// cfg.SetErrorSwitchingThreshold(1)

	client := ncsdk.NewAPIClient(cfg)
	ctx := context.Background()

	req := ncsdk.NewAccessTokenIssueRequest("user_123", "Alice")
	req.SetAvatarUrl("https://example.com/avatar.png")

	resp, httpResp, err := client.UserManagementAPI.
		IssueAccessToken(ctx).
		AccessTokenIssueRequest(*req).
		Execute()
	if err != nil {
		log.Fatalf("issue token failed: %v", err)
	}

	fmt.Println(httpResp.Status)
	fmt.Printf("%+v\n", resp)
}
```

## Error Handling

API errors are returned as `*GenericOpenAPIError` values. The error struct provides methods to access the HTTP status, business error code, and error message parsed from the response body.

```go
import (
	"errors"
	"fmt"

	ncsdk "github.com/NexconnAI-Dev/nexconn-server-sdk-go"
)

resp, httpResp, err := client.GroupChannelManagementAPI.
	CreateGroup(ctx).
	GroupChannelCreateRequest(req).
	Execute()
if err != nil {
	var apiErr *ncsdk.GenericOpenAPIError
	if errors.As(err, &apiErr) {
		fmt.Printf("HTTP %d: errorCode=%d, errorMessage=%s\n",
			apiErr.HttpStatus(), apiErr.ErrorCode(), apiErr.ErrorMessage())

		switch {
		case apiErr.IsBadRequest():
			// HTTP 400 — invalid parameters
		case apiErr.IsUnauthorized():
			// HTTP 401 — check your AppKey / AppSecret
		case apiErr.IsForbidden():
			// HTTP 403 — permission denied
		case apiErr.IsNotFound():
			// HTTP 404 — resource not found
		case apiErr.IsConflict():
			// HTTP 409 — resource already exists
		case apiErr.IsTooManyRequests():
			// HTTP 429 — rate limited, retry later
		case apiErr.IsServerError():
			// HTTP 5xx — server error, may retry
		}
	}
}
```

`GenericOpenAPIError` provides the following methods:

| Method | Description |
|--------|-------------|
| `HttpStatus()` | HTTP status code |
| `ErrorCode()` | Business error code from response body `code` field (`-1` if unparseable) |
| `ErrorMessage()` | Business error message from response body `errorMessage` field |
| `Body()` | Raw response body bytes |
| `Error()` | HTTP status text |
| `IsBadRequest()` | `true` if HTTP 400 |
| `IsUnauthorized()` | `true` if HTTP 401 |
| `IsForbidden()` | `true` if HTTP 403 |
| `IsNotFound()` | `true` if HTTP 404 |
| `IsConflict()` | `true` if HTTP 409 |
| `IsTooManyRequests()` | `true` if HTTP 429 |
| `IsServerError()` | `true` if HTTP 5xx |

## Features

- Automatic Nexconn request signing when `SetNexconnCredentials()` is configured
- Built-in multi-domain failover support via `SetPrimaryBackupDomains()`
- Default `User-Agent`: `ncsdk/0.1.1`
- Automatic `X-Request-ID` generation

## Configuration of Server URL

The SDK does not embed any default API domain. You must call `SetPrimaryBackupDomains()` before sending requests.

### Select Server Configuration

For using other server than the one defined on index 0 set context value `ncsdk.ContextServerIndex` of type `int`.

```go
ctx := context.WithValue(context.Background(), ncsdk.ContextServerIndex, 1)
```

## Documentation for API Endpoints

All requests use the primary/backup domains configured by the caller.

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChannelManagementAPI* | [**AddTagToChannels**](docs/ChannelManagementAPI.md#addtagtochannels) | **Post** /v4/channel/tag/add | Add tag to channel
*ChannelManagementAPI* | [**AddUserChannelTags**](docs/ChannelManagementAPI.md#adduserchanneltags) | **Post** /v4/user/channel/tag/add | Add user channel tag
*ChannelManagementAPI* | [**GetChannelAttribute**](docs/ChannelManagementAPI.md#getchannelattribute) | **Post** /v4/channel/attribute/get | Get channel attributes
*ChannelManagementAPI* | [**GetChannelPushNotification**](docs/ChannelManagementAPI.md#getchannelpushnotification) | **Post** /v4/channel/push/get | Get channel DND
*ChannelManagementAPI* | [**GetChannelTypeNotification**](docs/ChannelManagementAPI.md#getchanneltypenotification) | **Post** /v4/channel-type/push/get | Get DND by channel type
*ChannelManagementAPI* | [**ListChannelsByTag**](docs/ChannelManagementAPI.md#listchannelsbytag) | **Post** /v4/channel/tag/list | Get channels by tag
*ChannelManagementAPI* | [**ListUserChannelTags**](docs/ChannelManagementAPI.md#listuserchanneltags) | **Post** /v4/user/channel/tag/list | List user channel tags
*ChannelManagementAPI* | [**RemoveTagFromChannels**](docs/ChannelManagementAPI.md#removetagfromchannels) | **Post** /v4/channel/tag/delete | Remove tag from channel
*ChannelManagementAPI* | [**RemoveUserChannelTags**](docs/ChannelManagementAPI.md#removeuserchanneltags) | **Post** /v4/user/channel/tag/remove | Remove user channel tag
*ChannelManagementAPI* | [**SetChannelPin**](docs/ChannelManagementAPI.md#setchannelpin) | **Post** /v4/channel/pin/set | Pin a channel
*ChannelManagementAPI* | [**SetChannelPushNotification**](docs/ChannelManagementAPI.md#setchannelpushnotification) | **Post** /v4/channel/push/set | Set channel DND
*ChannelManagementAPI* | [**SetChannelTypeNotification**](docs/ChannelManagementAPI.md#setchanneltypenotification) | **Post** /v4/channel-type/push/set | Set DND by channel type
*CommunityChannelManagementAPI* | [**AddCommunityChannelUserGroupUsers**](docs/CommunityChannelManagementAPI.md#addcommunitychannelusergroupusers) | **Post** /v4/community-channel/user-group/user/add | Add community channel user group users
*CommunityChannelManagementAPI* | [**AddCommunityChannelUserGroups**](docs/CommunityChannelManagementAPI.md#addcommunitychannelusergroups) | **Post** /v4/community-channel/user-group/add | Add community channel user groups
*CommunityChannelManagementAPI* | [**AddPrivateSubchannelMembers**](docs/CommunityChannelManagementAPI.md#addprivatesubchannelmembers) | **Post** /v4/community-channel/private-subchannel/member/add | Add private subchannel members
*CommunityChannelManagementAPI* | [**BindCommunityChannelUserGroup**](docs/CommunityChannelManagementAPI.md#bindcommunitychannelusergroup) | **Post** /v4/community-channel/channel/user-group/bind | Bind community channel user group
*CommunityChannelManagementAPI* | [**CheckCommunityChannelMemberExist**](docs/CommunityChannelManagementAPI.md#checkcommunitychannelmemberexist) | **Post** /v4/community-channel/member/exist | Check community channel member exist
*CommunityChannelManagementAPI* | [**CreateCommunityChannel**](docs/CommunityChannelManagementAPI.md#createcommunitychannel) | **Post** /v4/community-channel/create | Create community channel
*CommunityChannelManagementAPI* | [**CreateCommunitySubchannel**](docs/CommunityChannelManagementAPI.md#createcommunitysubchannel) | **Post** /v4/community-channel/subchannel/create | Create community subchannel
*CommunityChannelManagementAPI* | [**DeleteCommunitySubchannel**](docs/CommunityChannelManagementAPI.md#deletecommunitysubchannel) | **Post** /v4/community-channel/subchannel/delete | Delete community subchannel
*CommunityChannelManagementAPI* | [**DismissCommunityChannel**](docs/CommunityChannelManagementAPI.md#dismisscommunitychannel) | **Post** /v4/community-channel/dismiss | Dismiss community channel
*CommunityChannelManagementAPI* | [**JoinCommunityChannel**](docs/CommunityChannelManagementAPI.md#joincommunitychannel) | **Post** /v4/community-channel/join | Join community channel
*CommunityChannelManagementAPI* | [**ListCommunityChannelHistoryMessages**](docs/CommunityChannelManagementAPI.md#listcommunitychannelhistorymessages) | **Post** /v4/community-channel/history-message/list | List community-channel history messages
*CommunityChannelManagementAPI* | [**ListCommunityChannelSubchannelUserGroups**](docs/CommunityChannelManagementAPI.md#listcommunitychannelsubchannelusergroups) | **Post** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups
*CommunityChannelManagementAPI* | [**ListCommunityChannelUserGroupSubchannels**](docs/CommunityChannelManagementAPI.md#listcommunitychannelusergroupsubchannels) | **Post** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels
*CommunityChannelManagementAPI* | [**ListCommunityChannelUserGroups**](docs/CommunityChannelManagementAPI.md#listcommunitychannelusergroups) | **Post** /v4/community-channel/user-group/list | List community channel user groups
*CommunityChannelManagementAPI* | [**ListCommunityChannelUserUserGroups**](docs/CommunityChannelManagementAPI.md#listcommunitychanneluserusergroups) | **Post** /v4/community-channel/user/user-group/list | List community channel user user groups
*CommunityChannelManagementAPI* | [**ListCommunitySubchannels**](docs/CommunityChannelManagementAPI.md#listcommunitysubchannels) | **Post** /v4/community-channel/subchannel/list | List community subchannels
*CommunityChannelManagementAPI* | [**ListCommunityUserSubchannels**](docs/CommunityChannelManagementAPI.md#listcommunityusersubchannels) | **Post** /v4/community-channel/user/subchannel/list | List community user subchannels
*CommunityChannelManagementAPI* | [**ListPrivateSubchannelMembers**](docs/CommunityChannelManagementAPI.md#listprivatesubchannelmembers) | **Post** /v4/community-channel/private-subchannel/member/list | List private subchannel members
*CommunityChannelManagementAPI* | [**QuitCommunityChannel**](docs/CommunityChannelManagementAPI.md#quitcommunitychannel) | **Post** /v4/community-channel/leave | Leave community channel
*CommunityChannelManagementAPI* | [**RemoveCommunityChannelUserGroupUsers**](docs/CommunityChannelManagementAPI.md#removecommunitychannelusergroupusers) | **Post** /v4/community-channel/user-group/user/remove | Remove community channel user group users
*CommunityChannelManagementAPI* | [**RemoveCommunityChannelUserGroups**](docs/CommunityChannelManagementAPI.md#removecommunitychannelusergroups) | **Post** /v4/community-channel/user-group/remove | Delete community channel user groups
*CommunityChannelManagementAPI* | [**RemovePrivateSubchannelMembers**](docs/CommunityChannelManagementAPI.md#removeprivatesubchannelmembers) | **Post** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members
*CommunityChannelManagementAPI* | [**UnbindCommunityChannelUserGroup**](docs/CommunityChannelManagementAPI.md#unbindcommunitychannelusergroup) | **Post** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group
*CommunityChannelManagementAPI* | [**UpdateCommunityChannelInfo**](docs/CommunityChannelManagementAPI.md#updatecommunitychannelinfo) | **Post** /v4/community-channel/update | Update community channel info
*CommunityChannelManagementAPI* | [**UpdateCommunitySubchannelType**](docs/CommunityChannelManagementAPI.md#updatecommunitysubchanneltype) | **Post** /v4/community-channel/subchannel-type/update | Update community subchannel type
*CommunityChannelModerationAPI* | [**AddCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationAPI.md#addcommunitychannelallowedsenderlist) | **Post** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list
*CommunityChannelModerationAPI* | [**AddCommunityChannelMutedUsers**](docs/CommunityChannelModerationAPI.md#addcommunitychannelmutedusers) | **Post** /v4/community-channel/mute-list/add | Add community-channel muted users
*CommunityChannelModerationAPI* | [**GetCommunityChannelFreezeList**](docs/CommunityChannelModerationAPI.md#getcommunitychannelfreezelist) | **Post** /v4/community-channel/freeze-list/get | Get community channel freeze status
*CommunityChannelModerationAPI* | [**ListCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationAPI.md#listcommunitychannelallowedsenderlist) | **Post** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list
*CommunityChannelModerationAPI* | [**ListCommunityChannelMutedUsers**](docs/CommunityChannelModerationAPI.md#listcommunitychannelmutedusers) | **Post** /v4/community-channel/mute-list/get | List community-channel muted users
*CommunityChannelModerationAPI* | [**RemoveCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationAPI.md#removecommunitychannelallowedsenderlist) | **Post** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list
*CommunityChannelModerationAPI* | [**RemoveCommunityChannelMutedUsers**](docs/CommunityChannelModerationAPI.md#removecommunitychannelmutedusers) | **Post** /v4/community-channel/mute-list/remove | Remove community-channel muted users
*CommunityChannelModerationAPI* | [**SetCommunityChannelFreezeList**](docs/CommunityChannelModerationAPI.md#setcommunitychannelfreezelist) | **Post** /v4/community-channel/freeze-list/set | Set community channel freeze list
*FriendshipAPI* | [**AddFriend**](docs/FriendshipAPI.md#addfriend) | **Post** /v4/friend/add | Add friend
*FriendshipAPI* | [**GetFriendPermission**](docs/FriendshipAPI.md#getfriendpermission) | **Post** /v4/friend/permission/get | Get friend permission
*FriendshipAPI* | [**GetFriendRelationships**](docs/FriendshipAPI.md#getfriendrelationships) | **Post** /v4/friend/relationship/get | Get friend relationships
*FriendshipAPI* | [**ListFriends**](docs/FriendshipAPI.md#listfriends) | **Post** /v4/friend/list | List friends
*FriendshipAPI* | [**RemoveAllFriends**](docs/FriendshipAPI.md#removeallfriends) | **Post** /v4/friend/remove-all | Clean all friends
*FriendshipAPI* | [**RemoveFriends**](docs/FriendshipAPI.md#removefriends) | **Post** /v4/friend/remove | Delete friends
*FriendshipAPI* | [**SetFriendPermission**](docs/FriendshipAPI.md#setfriendpermission) | **Post** /v4/friend/permission/set | Set friend permission
*FriendshipAPI* | [**SetFriendProfile**](docs/FriendshipAPI.md#setfriendprofile) | **Post** /v4/friend/profile/set | Set friend profile
*GroupChannelManagementAPI* | [**AddGroupChannelAdmins**](docs/GroupChannelManagementAPI.md#addgroupchanneladmins) | **Post** /v4/group-channel/admin/add | Add group admins
*GroupChannelManagementAPI* | [**AddGroupChannelMemberFavorites**](docs/GroupChannelManagementAPI.md#addgroupchannelmemberfavorites) | **Post** /v4/group-channel/member/favorites/add | Add favorite group members
*GroupChannelManagementAPI* | [**BatchGetGroupChannelMembers**](docs/GroupChannelManagementAPI.md#batchgetgroupchannelmembers) | **Post** /v4/group-channel/member/batch/get | Get specific group members
*GroupChannelManagementAPI* | [**BatchGetGroupChannelProfiles**](docs/GroupChannelManagementAPI.md#batchgetgroupchannelprofiles) | **Post** /v4/group-channel/profile/list | List group profiles
*GroupChannelManagementAPI* | [**CreateGroupChannel**](docs/GroupChannelManagementAPI.md#creategroupchannel) | **Post** /v4/group-channel/create | Create a group
*GroupChannelManagementAPI* | [**DeleteGroupChannelAlias**](docs/GroupChannelManagementAPI.md#deletegroupchannelalias) | **Post** /v4/group-channel/alias/delete | Delete group alias
*GroupChannelManagementAPI* | [**DismissGroupChannel**](docs/GroupChannelManagementAPI.md#dismissgroupchannel) | **Post** /v4/group-channel/dismiss | Dismiss a group
*GroupChannelManagementAPI* | [**GetGroupChannelAlias**](docs/GroupChannelManagementAPI.md#getgroupchannelalias) | **Post** /v4/group-channel/alias/get | Get group alias
*GroupChannelManagementAPI* | [**JoinGroupChannel**](docs/GroupChannelManagementAPI.md#joingroupchannel) | **Post** /v4/group-channel/join | Join a group
*GroupChannelManagementAPI* | [**KickUserFromAllGroupChannels**](docs/GroupChannelManagementAPI.md#kickuserfromallgroupchannels) | **Post** /v4/group-channel/member/kickout-all | Remove a user from all groups
*GroupChannelManagementAPI* | [**ListGroupChannelMemberFavorites**](docs/GroupChannelManagementAPI.md#listgroupchannelmemberfavorites) | **Post** /v4/group-channel/member/favorites/list | List favorite group members
*GroupChannelManagementAPI* | [**ListGroupChannelMembers**](docs/GroupChannelManagementAPI.md#listgroupchannelmembers) | **Post** /v4/group-channel/member/list | Query group members
*GroupChannelManagementAPI* | [**ListGroupChannels**](docs/GroupChannelManagementAPI.md#listgroupchannels) | **Post** /v4/group-channel/list | List group channels
*GroupChannelManagementAPI* | [**ListUserJoinedGroupChannels**](docs/GroupChannelManagementAPI.md#listuserjoinedgroupchannels) | **Post** /v4/group-channel/joined/list | Query user&#39;s groups
*GroupChannelManagementAPI* | [**QuitGroupChannel**](docs/GroupChannelManagementAPI.md#quitgroupchannel) | **Post** /v4/group-channel/leave | Leave a group
*GroupChannelManagementAPI* | [**RemoveGroupChannelAdmins**](docs/GroupChannelManagementAPI.md#removegroupchanneladmins) | **Post** /v4/group-channel/admin/remove | Remove group admins
*GroupChannelManagementAPI* | [**RemoveGroupChannelMemberFavorites**](docs/GroupChannelManagementAPI.md#removegroupchannelmemberfavorites) | **Post** /v4/group-channel/member/favorites/remove | Remove favorite group members
*GroupChannelManagementAPI* | [**SetGroupChannelAlias**](docs/GroupChannelManagementAPI.md#setgroupchannelalias) | **Post** /v4/group-channel/alias/set | Set group alias
*GroupChannelManagementAPI* | [**SetGroupChannelMember**](docs/GroupChannelManagementAPI.md#setgroupchannelmember) | **Post** /v4/group-channel/member/set | Set group member profile
*GroupChannelManagementAPI* | [**TransferGroupChannelOwner**](docs/GroupChannelManagementAPI.md#transfergroupchannelowner) | **Post** /v4/group-channel/transfer/owner | Transfer group ownership
*GroupChannelManagementAPI* | [**UpdateGroupChannelProfile**](docs/GroupChannelManagementAPI.md#updategroupchannelprofile) | **Post** /v4/group-channel/profile/update | Update group info
*GroupChannelModerationAPI* | [**AddGroupChannelAllowedSenderList**](docs/GroupChannelModerationAPI.md#addgroupchannelallowedsenderlist) | **Post** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list
*GroupChannelModerationAPI* | [**AddGroupChannelFreezeList**](docs/GroupChannelModerationAPI.md#addgroupchannelfreezelist) | **Post** /v4/group-channel/freeze-list/add | Freeze a group
*GroupChannelModerationAPI* | [**AddGroupChannelUserMuteList**](docs/GroupChannelModerationAPI.md#addgroupchannelusermutelist) | **Post** /v4/group-channel/user/mute-list/add | Mute a group member
*GroupChannelModerationAPI* | [**GetGroupChannelAllowedSenderList**](docs/GroupChannelModerationAPI.md#getgroupchannelallowedsenderlist) | **Post** /v4/group-channel/allowed-sender-list/get | Query allowed senders list
*GroupChannelModerationAPI* | [**GetGroupChannelFreezeList**](docs/GroupChannelModerationAPI.md#getgroupchannelfreezelist) | **Post** /v4/group-channel/freeze-list/get | Query group freeze status
*GroupChannelModerationAPI* | [**GetGroupChannelUserMuteList**](docs/GroupChannelModerationAPI.md#getgroupchannelusermutelist) | **Post** /v4/group-channel/user/mute-list/get | List muted group members
*GroupChannelModerationAPI* | [**RemoveGroupChannelAllowedSenderList**](docs/GroupChannelModerationAPI.md#removegroupchannelallowedsenderlist) | **Post** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list
*GroupChannelModerationAPI* | [**RemoveGroupChannelFreezeList**](docs/GroupChannelModerationAPI.md#removegroupchannelfreezelist) | **Post** /v4/group-channel/freeze-list/remove | Unfreeze a group
*GroupChannelModerationAPI* | [**RemoveGroupChannelUserMuteList**](docs/GroupChannelModerationAPI.md#removegroupchannelusermutelist) | **Post** /v4/group-channel/user/mute-list/remove | Unmute a group member
*MessageManagementAPI* | [**BroadcastOpenChannelMessage**](docs/MessageManagementAPI.md#broadcastopenchannelmessage) | **Post** /v4/open-channel/message/broadcast | Broadcast to all open channels
*MessageManagementAPI* | [**DeleteChannelMessageHistory**](docs/MessageManagementAPI.md#deletechannelmessagehistory) | **Post** /v4/channel/message/history/delete | Delete server-side channel message history
*MessageManagementAPI* | [**DeleteChannelTypeMessageMetadata**](docs/MessageManagementAPI.md#deletechanneltypemessagemetadata) | **Post** /v4/channel-type/message/metadata/delete | Delete message metadata
*MessageManagementAPI* | [**DeleteCommunityChannelMessageMetadata**](docs/MessageManagementAPI.md#deletecommunitychannelmessagemetadata) | **Post** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys
*MessageManagementAPI* | [**DeleteMessage**](docs/MessageManagementAPI.md#deletemessage) | **Post** /v4/message/delete | Delete a message (recall)
*MessageManagementAPI* | [**ListChannelTypeMessageMetadata**](docs/MessageManagementAPI.md#listchanneltypemessagemetadata) | **Post** /v4/channel-type/message/metadata/list | Get message metadata
*MessageManagementAPI* | [**ListCommunityChannelMessageMetadata**](docs/MessageManagementAPI.md#listcommunitychannelmessagemetadata) | **Post** /v4/community-channel/message/metadata/list | List community-channel message metadata
*MessageManagementAPI* | [**SendCommunityChannelMessage**](docs/MessageManagementAPI.md#sendcommunitychannelmessage) | **Post** /v4/community-channel/message/send | Send a community channel message
*MessageManagementAPI* | [**SendDirectChannelMessage**](docs/MessageManagementAPI.md#senddirectchannelmessage) | **Post** /v4/direct-channel/message/send | Send a direct message
*MessageManagementAPI* | [**SendDirectChannelStreamMessage**](docs/MessageManagementAPI.md#senddirectchannelstreammessage) | **Post** /v4/direct-channel/message/stream/send | Send a direct channel stream message
*MessageManagementAPI* | [**SendGroupChannelMessage**](docs/MessageManagementAPI.md#sendgroupchannelmessage) | **Post** /v4/group-channel/message/send | Send a group message
*MessageManagementAPI* | [**SendGroupChannelStreamMessage**](docs/MessageManagementAPI.md#sendgroupchannelstreammessage) | **Post** /v4/group-channel/message/stream/send | Send a group channel stream message
*MessageManagementAPI* | [**SendOpenChannelMessage**](docs/MessageManagementAPI.md#sendopenchannelmessage) | **Post** /v4/open-channel/message/send | Send an open channel message
*MessageManagementAPI* | [**SetChannelTypeMessageMetadata**](docs/MessageManagementAPI.md#setchanneltypemessagemetadata) | **Post** /v4/channel-type/message/metadata/set | Set message metadata
*MessageManagementAPI* | [**SetCommunityChannelMessageMetadata**](docs/MessageManagementAPI.md#setcommunitychannelmessagemetadata) | **Post** /v4/community-channel/message/metadata/set | Set community-channel message metadata
*MessageManagementAPI* | [**UpdateCommunityChannelMessage**](docs/MessageManagementAPI.md#updatecommunitychannelmessage) | **Post** /v4/community-channel/message/update | Update community-channel message
*MessageManagementAPI* | [**UpdateDirectChannelMessage**](docs/MessageManagementAPI.md#updatedirectchannelmessage) | **Post** /v4/direct-channel/message/update | Update direct-channel message
*MessageManagementAPI* | [**UpdateGroupChannelMessage**](docs/MessageManagementAPI.md#updategroupchannelmessage) | **Post** /v4/group-channel/message/update | Update group-channel message
*ModerationAPI* | [**BatchAddProfanityWords**](docs/ModerationAPI.md#batchaddprofanitywords) | **Post** /v4/profanity-word/batch/add | Batch add profanity words
*ModerationAPI* | [**BatchRemoveProfanityWords**](docs/ModerationAPI.md#batchremoveprofanitywords) | **Post** /v4/profanity-word/batch/remove | Batch delete profanity words
*ModerationAPI* | [**ListProfanityWords**](docs/ModerationAPI.md#listprofanitywords) | **Post** /v4/profanity-word/list | List profanity words
*ModerationAPI* | [**RemoveProfanityWord**](docs/ModerationAPI.md#removeprofanityword) | **Post** /v4/profanity-word/remove | Delete profanity word
*OpenChannelManagementAPI* | [**CreateOpenChannel**](docs/OpenChannelManagementAPI.md#createopenchannel) | **Post** /v4/open-channel/create | Create an open channel
*OpenChannelManagementAPI* | [**DestroyOpenChannels**](docs/OpenChannelManagementAPI.md#destroyopenchannels) | **Post** /v4/open-channel/destroy | Destroy an open channel
*OpenChannelManagementAPI* | [**GetOpenChannel**](docs/OpenChannelManagementAPI.md#getopenchannel) | **Post** /v4/open-channel/get | Get open channel info
*OpenChannelManagementAPI* | [**SetOpenChannelDestroyType**](docs/OpenChannelManagementAPI.md#setopenchanneldestroytype) | **Post** /v4/open-channel/destroy-type/set | Set auto-destroy type
*OpenChannelMessagePriorityAPI* | [**AddOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityAPI.md#addopenchannellowprioritymessagetypelist) | **Post** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types
*OpenChannelMessagePriorityAPI* | [**GetOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityAPI.md#getopenchannellowprioritymessagetypelist) | **Post** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types
*OpenChannelMessagePriorityAPI* | [**RemoveOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityAPI.md#removeopenchannellowprioritymessagetypelist) | **Post** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types
*OpenChannelMetadataAPI* | [**BatchGetOpenChannelMetadata**](docs/OpenChannelMetadataAPI.md#batchgetopenchannelmetadata) | **Post** /v4/open-channel/metadata/batch/get | Query metadata
*OpenChannelMetadataAPI* | [**BatchRemoveOpenChannelMetadata**](docs/OpenChannelMetadataAPI.md#batchremoveopenchannelmetadata) | **Post** /v4/open-channel/metadata/batch/remove | Batch delete metadata
*OpenChannelMetadataAPI* | [**BatchSetOpenChannelMetadata**](docs/OpenChannelMetadataAPI.md#batchsetopenchannelmetadata) | **Post** /v4/open-channel/metadata/batch/set | Batch set metadata
*OpenChannelParticipantsModerationAPI* | [**AddOpenChannelFreezeList**](docs/OpenChannelParticipantsModerationAPI.md#addopenchannelfreezelist) | **Post** /v4/open-channel/freeze-list/add | Freeze an open channel
*OpenChannelParticipantsModerationAPI* | [**AddOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationAPI.md#addopenchannelglobalmutelist) | **Post** /v4/open-channel/global-mute-list/add | Mute a user globally
*OpenChannelParticipantsModerationAPI* | [**AddOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationAPI.md#addopenchannelparticipantallowedsenderlist) | **Post** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list
*OpenChannelParticipantsModerationAPI* | [**AddOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationAPI.md#addopenchannelparticipantbanlist) | **Post** /v4/open-channel/participant/ban-list/add | Ban a participant
*OpenChannelParticipantsModerationAPI* | [**AddOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationAPI.md#addopenchannelparticipantmutelist) | **Post** /v4/open-channel/participant/mute-list/add | Mute a participant
*OpenChannelParticipantsModerationAPI* | [**CheckOpenChannelFreeze**](docs/OpenChannelParticipantsModerationAPI.md#checkopenchannelfreeze) | **Post** /v4/open-channel/freeze/check | Check open channel freeze status
*OpenChannelParticipantsModerationAPI* | [**CheckOpenChannelParticipantsExist**](docs/OpenChannelParticipantsModerationAPI.md#checkopenchannelparticipantsexist) | **Post** /v4/open-channel/participant/exist | Batch check participants
*OpenChannelParticipantsModerationAPI* | [**GetOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationAPI.md#getopenchannelglobalmutelist) | **Post** /v4/open-channel/global-mute-list/get | List globally muted users
*OpenChannelParticipantsModerationAPI* | [**GetOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationAPI.md#getopenchannelparticipantallowedsenderlist) | **Post** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list
*OpenChannelParticipantsModerationAPI* | [**GetOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationAPI.md#getopenchannelparticipantbanlist) | **Post** /v4/open-channel/participant/ban-list/get | List banned participants
*OpenChannelParticipantsModerationAPI* | [**GetOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationAPI.md#getopenchannelparticipantmutelist) | **Post** /v4/open-channel/participant/mute-list/get | List muted participants
*OpenChannelParticipantsModerationAPI* | [**ListFrozenOpenChannels**](docs/OpenChannelParticipantsModerationAPI.md#listfrozenopenchannels) | **Post** /v4/open-channel/freeze-list/get | List frozen open channels
*OpenChannelParticipantsModerationAPI* | [**ListOpenChannelParticipants**](docs/OpenChannelParticipantsModerationAPI.md#listopenchannelparticipants) | **Post** /v4/open-channel/participant/list | List participants
*OpenChannelParticipantsModerationAPI* | [**RemoveOpenChannelFreezeList**](docs/OpenChannelParticipantsModerationAPI.md#removeopenchannelfreezelist) | **Post** /v4/open-channel/freeze-list/remove | Unfreeze an open channel
*OpenChannelParticipantsModerationAPI* | [**RemoveOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationAPI.md#removeopenchannelglobalmutelist) | **Post** /v4/open-channel/global-mute-list/remove | Unmute a user globally
*OpenChannelParticipantsModerationAPI* | [**RemoveOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationAPI.md#removeopenchannelparticipantallowedsenderlist) | **Post** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list
*OpenChannelParticipantsModerationAPI* | [**RemoveOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationAPI.md#removeopenchannelparticipantbanlist) | **Post** /v4/open-channel/participant/ban-list/remove | Unban a participant
*OpenChannelParticipantsModerationAPI* | [**RemoveOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationAPI.md#removeopenchannelparticipantmutelist) | **Post** /v4/open-channel/participant/mute-list/remove | Unmute a participant
*OpenChannelPriorityControlsAPI* | [**AddOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsAPI.md#addopenchannelprioritymessagetypelist) | **Post** /v4/open-channel/priority-message-type-list/add | Add priority message types
*OpenChannelPriorityControlsAPI* | [**AddOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsAPI.md#addopenchannelprioritysenderlist) | **Post** /v4/open-channel/priority-sender-list/add | Add priority senders
*OpenChannelPriorityControlsAPI* | [**GetOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsAPI.md#getopenchannelprioritymessagetypelist) | **Post** /v4/open-channel/priority-message-type-list/get | Query priority message types
*OpenChannelPriorityControlsAPI* | [**GetOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsAPI.md#getopenchannelprioritysenderlist) | **Post** /v4/open-channel/priority-sender-list/get | Query priority senders
*OpenChannelPriorityControlsAPI* | [**RemoveOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsAPI.md#removeopenchannelprioritymessagetypelist) | **Post** /v4/open-channel/priority-message-type-list/remove | Remove priority message types
*OpenChannelPriorityControlsAPI* | [**RemoveOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsAPI.md#removeopenchannelprioritysenderlist) | **Post** /v4/open-channel/priority-sender-list/remove | Remove priority senders
*SystemMessagesAPI* | [**BroadcastMessageOnline**](docs/SystemMessagesAPI.md#broadcastmessageonline) | **Post** /v4/system-channel/message/broadcast-online | Broadcast to online users
*SystemMessagesAPI* | [**BroadcastSystemChannelMessage**](docs/SystemMessagesAPI.md#broadcastsystemchannelmessage) | **Post** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent)
*SystemMessagesAPI* | [**DeleteBroadcastMessage**](docs/SystemMessagesAPI.md#deletebroadcastmessage) | **Post** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users
*SystemMessagesAPI* | [**SendSystemChannelMessage**](docs/SystemMessagesAPI.md#sendsystemchannelmessage) | **Post** /v4/system-channel/message/send | Send a system message
*SystemMessagesAPI* | [**SendSystemChannelPushByPackage**](docs/SystemMessagesAPI.md#sendsystemchannelpushbypackage) | **Post** /v4/system-channel/app-package-users/send | Push by app package name
*SystemMessagesAPI* | [**SendSystemChannelPushByTag**](docs/SystemMessagesAPI.md#sendsystemchannelpushbytag) | **Post** /v4/system-channel/tagged-users/send | Push to tagged users
*UserBlocklistAPI* | [**AddUserBlocklist**](docs/UserBlocklistAPI.md#adduserblocklist) | **Post** /v4/user/blocklist/add | Add to blocklist
*UserBlocklistAPI* | [**GetUserBlocklist**](docs/UserBlocklistAPI.md#getuserblocklist) | **Post** /v4/user/blocklist/get | Get blocklist
*UserBlocklistAPI* | [**RemoveUserBlocklist**](docs/UserBlocklistAPI.md#removeuserblocklist) | **Post** /v4/user/blocklist/remove | Remove from blocklist
*UserManagementAPI* | [**BanUsers**](docs/UserManagementAPI.md#banusers) | **Post** /v4/user/ban | Ban a user
*UserManagementAPI* | [**BatchGetUserTags**](docs/UserManagementAPI.md#batchgetusertags) | **Post** /v4/user/tag/batch/get | Get user tags
*UserManagementAPI* | [**BatchSetUserTags**](docs/UserManagementAPI.md#batchsetusertags) | **Post** /v4/user/tag/batch/set | Batch set user tags
*UserManagementAPI* | [**ExpireAccessToken**](docs/UserManagementAPI.md#expireaccesstoken) | **Post** /v4/auth/access-token/expire | Expire an access token
*UserManagementAPI* | [**GetUser**](docs/UserManagementAPI.md#getuser) | **Post** /v4/user/get | Get user info
*UserManagementAPI* | [**GetUserConnectionStatus**](docs/UserManagementAPI.md#getuserconnectionstatus) | **Post** /v4/user/connection-status/get | Check user online status
*UserManagementAPI* | [**IssueAccessToken**](docs/UserManagementAPI.md#issueaccesstoken) | **Post** /v4/auth/access-token/issue | Register a user
*UserManagementAPI* | [**ListBannedUsers**](docs/UserManagementAPI.md#listbannedusers) | **Post** /v4/user/ban/list | List banned users
*UserManagementAPI* | [**ListChannelTypeMute**](docs/UserManagementAPI.md#listchanneltypemute) | **Post** /v4/channel-type/mute/list | List muted direct channel users
*UserManagementAPI* | [**ListSoftDeletedUsers**](docs/UserManagementAPI.md#listsoftdeletedusers) | **Post** /v4/user/soft-deleted/list | Query soft-deleted users
*UserManagementAPI* | [**RestoreUsers**](docs/UserManagementAPI.md#restoreusers) | **Post** /v4/user/restore | Restore a user
*UserManagementAPI* | [**SetChannelTypeMute**](docs/UserManagementAPI.md#setchanneltypemute) | **Post** /v4/channel-type/mute/set | Mute a user in direct channels
*UserManagementAPI* | [**SoftDeleteUsers**](docs/UserManagementAPI.md#softdeleteusers) | **Post** /v4/user/soft-delete | Soft-delete a user
*UserManagementAPI* | [**UnbanUsers**](docs/UserManagementAPI.md#unbanusers) | **Post** /v4/user/unban | Unban a user
*UserManagementAPI* | [**UpdateUser**](docs/UserManagementAPI.md#updateuser) | **Post** /v4/user/update | Update user info
*UserProfileHostingAPI* | [**BatchGetUserProfiles**](docs/UserProfileHostingAPI.md#batchgetuserprofiles) | **Post** /v4/user/profile/batch/get | Batch get user profiles
*UserProfileHostingAPI* | [**DeleteUserProfiles**](docs/UserProfileHostingAPI.md#deleteuserprofiles) | **Post** /v4/user/profile/delete | Clear user profiles
*UserProfileHostingAPI* | [**ListUserProfiles**](docs/UserProfileHostingAPI.md#listuserprofiles) | **Post** /v4/user/profile/list | List user profiles
*UserProfileHostingAPI* | [**SetUserProfile**](docs/UserProfileHostingAPI.md#setuserprofile) | **Post** /v4/user/profile/set | Set user profile


## Documentation For Models

- [AccessTokenExpireRequest](docs/AccessTokenExpireRequest.md)
- [AccessTokenIssueRequest](docs/AccessTokenIssueRequest.md)
- [AccessTokenIssueResponse](docs/AccessTokenIssueResponse.md)
- [AccessTokenIssueResult](docs/AccessTokenIssueResult.md)
- [BannedUser](docs/BannedUser.md)
- [ChannelAttributeGetRequest](docs/ChannelAttributeGetRequest.md)
- [ChannelAttributeGetResponse](docs/ChannelAttributeGetResponse.md)
- [ChannelAttributeGetResponseResult](docs/ChannelAttributeGetResponseResult.md)
- [ChannelAttributeTagItem](docs/ChannelAttributeTagItem.md)
- [ChannelMessageHistoryDeleteRequest](docs/ChannelMessageHistoryDeleteRequest.md)
- [ChannelMessageSendResponse](docs/ChannelMessageSendResponse.md)
- [ChannelMessageSendResponseResult](docs/ChannelMessageSendResponseResult.md)
- [ChannelNotificationState](docs/ChannelNotificationState.md)
- [ChannelPinSetRequest](docs/ChannelPinSetRequest.md)
- [ChannelPinState](docs/ChannelPinState.md)
- [ChannelPushGetRequest](docs/ChannelPushGetRequest.md)
- [ChannelPushGetResponse](docs/ChannelPushGetResponse.md)
- [ChannelPushGetResponseResult](docs/ChannelPushGetResponseResult.md)
- [ChannelPushSetRequest](docs/ChannelPushSetRequest.md)
- [ChannelTagAddRequest](docs/ChannelTagAddRequest.md)
- [ChannelTagListRequest](docs/ChannelTagListRequest.md)
- [ChannelTagListResponse](docs/ChannelTagListResponse.md)
- [ChannelTagListResponseResult](docs/ChannelTagListResponseResult.md)
- [ChannelTagRemoveRequest](docs/ChannelTagRemoveRequest.md)
- [ChannelTagTargetItem](docs/ChannelTagTargetItem.md)
- [ChannelTypeMessageMetadataDeleteRequest](docs/ChannelTypeMessageMetadataDeleteRequest.md)
- [ChannelTypeMessageMetadataListRequest](docs/ChannelTypeMessageMetadataListRequest.md)
- [ChannelTypeMessageMetadataListResponse](docs/ChannelTypeMessageMetadataListResponse.md)
- [ChannelTypeMessageMetadataListResponseResult](docs/ChannelTypeMessageMetadataListResponseResult.md)
- [ChannelTypeMuteListRequest](docs/ChannelTypeMuteListRequest.md)
- [ChannelTypeMuteListResponse](docs/ChannelTypeMuteListResponse.md)
- [ChannelTypeMuteListResponseResult](docs/ChannelTypeMuteListResponseResult.md)
- [ChannelTypeMuteSetRequest](docs/ChannelTypeMuteSetRequest.md)
- [ChannelTypeNotificationGetRequest](docs/ChannelTypeNotificationGetRequest.md)
- [ChannelTypeNotificationGetResponse](docs/ChannelTypeNotificationGetResponse.md)
- [ChannelTypeNotificationGetResponseResult](docs/ChannelTypeNotificationGetResponseResult.md)
- [ChannelTypeNotificationSetRequest](docs/ChannelTypeNotificationSetRequest.md)
- [CodeOnlyResponse](docs/CodeOnlyResponse.md)
- [CommunityChannelAllowedSenderItem](docs/CommunityChannelAllowedSenderItem.md)
- [CommunityChannelAllowedSenderListGetRequest](docs/CommunityChannelAllowedSenderListGetRequest.md)
- [CommunityChannelAllowedSenderListGetResponse](docs/CommunityChannelAllowedSenderListGetResponse.md)
- [CommunityChannelAllowedSenderListGetResponseResult](docs/CommunityChannelAllowedSenderListGetResponseResult.md)
- [CommunityChannelAllowedSenderListUpdateRequest](docs/CommunityChannelAllowedSenderListUpdateRequest.md)
- [CommunityChannelCreateRequest](docs/CommunityChannelCreateRequest.md)
- [CommunityChannelDismissRequest](docs/CommunityChannelDismissRequest.md)
- [CommunityChannelFreezeListGetRequest](docs/CommunityChannelFreezeListGetRequest.md)
- [CommunityChannelFreezeListGetResponse](docs/CommunityChannelFreezeListGetResponse.md)
- [CommunityChannelFreezeListGetResponseResult](docs/CommunityChannelFreezeListGetResponseResult.md)
- [CommunityChannelFreezeListSetRequest](docs/CommunityChannelFreezeListSetRequest.md)
- [CommunityChannelHistoryMessageListRequest](docs/CommunityChannelHistoryMessageListRequest.md)
- [CommunityChannelMemberExistResponse](docs/CommunityChannelMemberExistResponse.md)
- [CommunityChannelMemberExistResponseResult](docs/CommunityChannelMemberExistResponseResult.md)
- [CommunityChannelMemberRequest](docs/CommunityChannelMemberRequest.md)
- [CommunityChannelMessageMetadataDeleteRequest](docs/CommunityChannelMessageMetadataDeleteRequest.md)
- [CommunityChannelMessageMetadataListRequest](docs/CommunityChannelMessageMetadataListRequest.md)
- [CommunityChannelMessageMetadataListResponse](docs/CommunityChannelMessageMetadataListResponse.md)
- [CommunityChannelMessageMetadataListResponseResult](docs/CommunityChannelMessageMetadataListResponseResult.md)
- [CommunityChannelMessageMetadataSetRequest](docs/CommunityChannelMessageMetadataSetRequest.md)
- [CommunityChannelMessageSendRequest](docs/CommunityChannelMessageSendRequest.md)
- [CommunityChannelMessageUpdateRequest](docs/CommunityChannelMessageUpdateRequest.md)
- [CommunityChannelMuteListAddRequest](docs/CommunityChannelMuteListAddRequest.md)
- [CommunityChannelMuteListGetRequest](docs/CommunityChannelMuteListGetRequest.md)
- [CommunityChannelMuteListGetResponse](docs/CommunityChannelMuteListGetResponse.md)
- [CommunityChannelMuteListGetResponseResult](docs/CommunityChannelMuteListGetResponseResult.md)
- [CommunityChannelMuteListRemoveRequest](docs/CommunityChannelMuteListRemoveRequest.md)
- [CommunityChannelMutedMemberItem](docs/CommunityChannelMutedMemberItem.md)
- [CommunityChannelSubchannelUserGroupListRequest](docs/CommunityChannelSubchannelUserGroupListRequest.md)
- [CommunityChannelSubchannelUserGroupListResponse](docs/CommunityChannelSubchannelUserGroupListResponse.md)
- [CommunityChannelSubchannelUserGroupListResponseResult](docs/CommunityChannelSubchannelUserGroupListResponseResult.md)
- [CommunityChannelUpdateRequest](docs/CommunityChannelUpdateRequest.md)
- [CommunityChannelUserGroupAddRequest](docs/CommunityChannelUserGroupAddRequest.md)
- [CommunityChannelUserGroupBindingRequest](docs/CommunityChannelUserGroupBindingRequest.md)
- [CommunityChannelUserGroupDeleteRequest](docs/CommunityChannelUserGroupDeleteRequest.md)
- [CommunityChannelUserGroupItem](docs/CommunityChannelUserGroupItem.md)
- [CommunityChannelUserGroupListRequest](docs/CommunityChannelUserGroupListRequest.md)
- [CommunityChannelUserGroupListResponse](docs/CommunityChannelUserGroupListResponse.md)
- [CommunityChannelUserGroupListResponseResult](docs/CommunityChannelUserGroupListResponseResult.md)
- [CommunityChannelUserGroupSubchannelListRequest](docs/CommunityChannelUserGroupSubchannelListRequest.md)
- [CommunityChannelUserGroupSubchannelListResponse](docs/CommunityChannelUserGroupSubchannelListResponse.md)
- [CommunityChannelUserGroupSubchannelListResponseResult](docs/CommunityChannelUserGroupSubchannelListResponseResult.md)
- [CommunityChannelUserGroupUsersRequest](docs/CommunityChannelUserGroupUsersRequest.md)
- [CommunityChannelUserUserGroupListRequest](docs/CommunityChannelUserUserGroupListRequest.md)
- [CommunityChannelUserUserGroupListResponse](docs/CommunityChannelUserUserGroupListResponse.md)
- [CommunityChannelUserUserGroupListResponseResult](docs/CommunityChannelUserUserGroupListResponseResult.md)
- [CommunityPrivateSubchannelMemberListRequest](docs/CommunityPrivateSubchannelMemberListRequest.md)
- [CommunityPrivateSubchannelMemberListResponse](docs/CommunityPrivateSubchannelMemberListResponse.md)
- [CommunityPrivateSubchannelMemberListResponseResult](docs/CommunityPrivateSubchannelMemberListResponseResult.md)
- [CommunityPrivateSubchannelMembersRequest](docs/CommunityPrivateSubchannelMembersRequest.md)
- [CommunitySubchannelCreateRequest](docs/CommunitySubchannelCreateRequest.md)
- [CommunitySubchannelItem](docs/CommunitySubchannelItem.md)
- [CommunitySubchannelKeyRequest](docs/CommunitySubchannelKeyRequest.md)
- [CommunitySubchannelListRequest](docs/CommunitySubchannelListRequest.md)
- [CommunitySubchannelListResponse](docs/CommunitySubchannelListResponse.md)
- [CommunitySubchannelListResponseResult](docs/CommunitySubchannelListResponseResult.md)
- [CommunitySubchannelTypeUpdateRequest](docs/CommunitySubchannelTypeUpdateRequest.md)
- [CommunityUserSubchannelListRequest](docs/CommunityUserSubchannelListRequest.md)
- [CommunityUserSubchannelListResponse](docs/CommunityUserSubchannelListResponse.md)
- [CommunityUserSubchannelListResponseResult](docs/CommunityUserSubchannelListResponseResult.md)
- [DirectChannelMessageSendRequest](docs/DirectChannelMessageSendRequest.md)
- [DirectChannelMessageUpdateRequest](docs/DirectChannelMessageUpdateRequest.md)
- [DirectChannelStreamMessageSendRequest](docs/DirectChannelStreamMessageSendRequest.md)
- [FriendAddRequest](docs/FriendAddRequest.md)
- [FriendCleanRequest](docs/FriendCleanRequest.md)
- [FriendDeleteRequest](docs/FriendDeleteRequest.md)
- [FriendItem](docs/FriendItem.md)
- [FriendListRequest](docs/FriendListRequest.md)
- [FriendListResponse](docs/FriendListResponse.md)
- [FriendListResponseResult](docs/FriendListResponseResult.md)
- [FriendPermissionGetRequest](docs/FriendPermissionGetRequest.md)
- [FriendPermissionGetResponse](docs/FriendPermissionGetResponse.md)
- [FriendPermissionGetResponseResult](docs/FriendPermissionGetResponseResult.md)
- [FriendPermissionItem](docs/FriendPermissionItem.md)
- [FriendPermissionSetRequest](docs/FriendPermissionSetRequest.md)
- [FriendProfileSetRequest](docs/FriendProfileSetRequest.md)
- [FriendRelationshipGetRequest](docs/FriendRelationshipGetRequest.md)
- [FriendRelationshipGetResponse](docs/FriendRelationshipGetResponse.md)
- [FriendRelationshipGetResponseResult](docs/FriendRelationshipGetResponseResult.md)
- [FriendRelationshipItem](docs/FriendRelationshipItem.md)
- [GroupChannelAdminUsersRequest](docs/GroupChannelAdminUsersRequest.md)
- [GroupChannelAliasGetRequest](docs/GroupChannelAliasGetRequest.md)
- [GroupChannelAliasGetResponse](docs/GroupChannelAliasGetResponse.md)
- [GroupChannelAliasGetResponseResult](docs/GroupChannelAliasGetResponseResult.md)
- [GroupChannelAliasSetRequest](docs/GroupChannelAliasSetRequest.md)
- [GroupChannelAllowedSenderListGetRequest](docs/GroupChannelAllowedSenderListGetRequest.md)
- [GroupChannelAllowedSenderListGetResponse](docs/GroupChannelAllowedSenderListGetResponse.md)
- [GroupChannelAllowedSenderListGetResponseResult](docs/GroupChannelAllowedSenderListGetResponseResult.md)
- [GroupChannelAllowedSenderListUpdateRequest](docs/GroupChannelAllowedSenderListUpdateRequest.md)
- [GroupChannelCreateRequest](docs/GroupChannelCreateRequest.md)
- [GroupChannelDismissRequest](docs/GroupChannelDismissRequest.md)
- [GroupChannelFavoriteItem](docs/GroupChannelFavoriteItem.md)
- [GroupChannelFreezeListGetRequest](docs/GroupChannelFreezeListGetRequest.md)
- [GroupChannelFreezeListGetResponse](docs/GroupChannelFreezeListGetResponse.md)
- [GroupChannelFreezeListGetResponseResult](docs/GroupChannelFreezeListGetResponseResult.md)
- [GroupChannelFreezeListUpdateRequest](docs/GroupChannelFreezeListUpdateRequest.md)
- [GroupChannelFreezeStatusItem](docs/GroupChannelFreezeStatusItem.md)
- [GroupChannelJoinRequest](docs/GroupChannelJoinRequest.md)
- [GroupChannelJoinResponse](docs/GroupChannelJoinResponse.md)
- [GroupChannelJoinedItem](docs/GroupChannelJoinedItem.md)
- [GroupChannelJoinedListRequest](docs/GroupChannelJoinedListRequest.md)
- [GroupChannelJoinedListResponse](docs/GroupChannelJoinedListResponse.md)
- [GroupChannelJoinedListResponseResult](docs/GroupChannelJoinedListResponseResult.md)
- [GroupChannelKickUserFromAllRequest](docs/GroupChannelKickUserFromAllRequest.md)
- [GroupChannelListRequest](docs/GroupChannelListRequest.md)
- [GroupChannelListResponse](docs/GroupChannelListResponse.md)
- [GroupChannelListResponseResult](docs/GroupChannelListResponseResult.md)
- [GroupChannelMemberBatchGetRequest](docs/GroupChannelMemberBatchGetRequest.md)
- [GroupChannelMemberBatchGetResponse](docs/GroupChannelMemberBatchGetResponse.md)
- [GroupChannelMemberBatchGetResponseResult](docs/GroupChannelMemberBatchGetResponseResult.md)
- [GroupChannelMemberFavoritesListRequest](docs/GroupChannelMemberFavoritesListRequest.md)
- [GroupChannelMemberFavoritesListResponse](docs/GroupChannelMemberFavoritesListResponse.md)
- [GroupChannelMemberFavoritesListResponseResult](docs/GroupChannelMemberFavoritesListResponseResult.md)
- [GroupChannelMemberFavoritesUpdateRequest](docs/GroupChannelMemberFavoritesUpdateRequest.md)
- [GroupChannelMemberItem](docs/GroupChannelMemberItem.md)
- [GroupChannelMemberListRequest](docs/GroupChannelMemberListRequest.md)
- [GroupChannelMemberListResponse](docs/GroupChannelMemberListResponse.md)
- [GroupChannelMemberListResponseResult](docs/GroupChannelMemberListResponseResult.md)
- [GroupChannelMemberSetRequest](docs/GroupChannelMemberSetRequest.md)
- [GroupChannelMessageSendRequest](docs/GroupChannelMessageSendRequest.md)
- [GroupChannelMessageUpdateRequest](docs/GroupChannelMessageUpdateRequest.md)
- [GroupChannelMutedMemberItem](docs/GroupChannelMutedMemberItem.md)
- [GroupChannelProfileItem](docs/GroupChannelProfileItem.md)
- [GroupChannelProfileListRequest](docs/GroupChannelProfileListRequest.md)
- [GroupChannelProfileListResponse](docs/GroupChannelProfileListResponse.md)
- [GroupChannelProfileListResponseResult](docs/GroupChannelProfileListResponseResult.md)
- [GroupChannelProfileUpdateRequest](docs/GroupChannelProfileUpdateRequest.md)
- [GroupChannelQuitRequest](docs/GroupChannelQuitRequest.md)
- [GroupChannelStreamMessageSendRequest](docs/GroupChannelStreamMessageSendRequest.md)
- [GroupChannelSummaryItem](docs/GroupChannelSummaryItem.md)
- [GroupChannelTransferOwnerRequest](docs/GroupChannelTransferOwnerRequest.md)
- [GroupChannelUserMuteListAddRequest](docs/GroupChannelUserMuteListAddRequest.md)
- [GroupChannelUserMuteListGetRequest](docs/GroupChannelUserMuteListGetRequest.md)
- [GroupChannelUserMuteListGetResponse](docs/GroupChannelUserMuteListGetResponse.md)
- [GroupChannelUserMuteListGetResponseResult](docs/GroupChannelUserMuteListGetResponseResult.md)
- [GroupChannelUserMuteListRemoveRequest](docs/GroupChannelUserMuteListRemoveRequest.md)
- [MessageChannelDelivery](docs/MessageChannelDelivery.md)
- [MessageDeleteRequest](docs/MessageDeleteRequest.md)
- [MessageHistoryResponse](docs/MessageHistoryResponse.md)
- [MessageHistoryResponseResult](docs/MessageHistoryResponseResult.md)
- [MessageMetadataListItem](docs/MessageMetadataListItem.md)
- [MessageMetadataSetRequest](docs/MessageMetadataSetRequest.md)
- [MessageRecord](docs/MessageRecord.md)
- [MessageUserDelivery](docs/MessageUserDelivery.md)
- [OpenChannelAllowedSenderListGetResponse](docs/OpenChannelAllowedSenderListGetResponse.md)
- [OpenChannelAllowedSenderListGetResponseResult](docs/OpenChannelAllowedSenderListGetResponseResult.md)
- [OpenChannelAllowedSenderListUpdateRequest](docs/OpenChannelAllowedSenderListUpdateRequest.md)
- [OpenChannelBannedParticipantItem](docs/OpenChannelBannedParticipantItem.md)
- [OpenChannelBroadcastRequest](docs/OpenChannelBroadcastRequest.md)
- [OpenChannelCreateRequest](docs/OpenChannelCreateRequest.md)
- [OpenChannelDestroyRequest](docs/OpenChannelDestroyRequest.md)
- [OpenChannelDestroyTypeSetRequest](docs/OpenChannelDestroyTypeSetRequest.md)
- [OpenChannelFreezeCheckRequest](docs/OpenChannelFreezeCheckRequest.md)
- [OpenChannelFreezeCheckResponse](docs/OpenChannelFreezeCheckResponse.md)
- [OpenChannelFreezeCheckResponseResult](docs/OpenChannelFreezeCheckResponseResult.md)
- [OpenChannelFreezeListGetRequest](docs/OpenChannelFreezeListGetRequest.md)
- [OpenChannelFreezeListGetResponse](docs/OpenChannelFreezeListGetResponse.md)
- [OpenChannelFreezeListGetResponseResult](docs/OpenChannelFreezeListGetResponseResult.md)
- [OpenChannelFreezeListUpdateRequest](docs/OpenChannelFreezeListUpdateRequest.md)
- [OpenChannelGetRequest](docs/OpenChannelGetRequest.md)
- [OpenChannelGetResponse](docs/OpenChannelGetResponse.md)
- [OpenChannelGetResponseResult](docs/OpenChannelGetResponseResult.md)
- [OpenChannelGlobalMuteListAddRequest](docs/OpenChannelGlobalMuteListAddRequest.md)
- [OpenChannelGlobalMuteListRemoveRequest](docs/OpenChannelGlobalMuteListRemoveRequest.md)
- [OpenChannelLowPriorityMessageTypeListRequest](docs/OpenChannelLowPriorityMessageTypeListRequest.md)
- [OpenChannelMessageSendRequest](docs/OpenChannelMessageSendRequest.md)
- [OpenChannelMessageTypeListResponse](docs/OpenChannelMessageTypeListResponse.md)
- [OpenChannelMessageTypeListResponseResult](docs/OpenChannelMessageTypeListResponseResult.md)
- [OpenChannelMetadataBatchGetRequest](docs/OpenChannelMetadataBatchGetRequest.md)
- [OpenChannelMetadataBatchGetResponse](docs/OpenChannelMetadataBatchGetResponse.md)
- [OpenChannelMetadataBatchGetResponseResult](docs/OpenChannelMetadataBatchGetResponseResult.md)
- [OpenChannelMetadataBatchRemoveRequest](docs/OpenChannelMetadataBatchRemoveRequest.md)
- [OpenChannelMetadataBatchSetRequest](docs/OpenChannelMetadataBatchSetRequest.md)
- [OpenChannelMetadataEntry](docs/OpenChannelMetadataEntry.md)
- [OpenChannelMutedParticipantItem](docs/OpenChannelMutedParticipantItem.md)
- [OpenChannelParticipantBanListGetResponse](docs/OpenChannelParticipantBanListGetResponse.md)
- [OpenChannelParticipantBanListGetResponseResult](docs/OpenChannelParticipantBanListGetResponseResult.md)
- [OpenChannelParticipantExistItem](docs/OpenChannelParticipantExistItem.md)
- [OpenChannelParticipantExistRequest](docs/OpenChannelParticipantExistRequest.md)
- [OpenChannelParticipantExistResponse](docs/OpenChannelParticipantExistResponse.md)
- [OpenChannelParticipantExistResponseResult](docs/OpenChannelParticipantExistResponseResult.md)
- [OpenChannelParticipantIdsRequest](docs/OpenChannelParticipantIdsRequest.md)
- [OpenChannelParticipantIdsResponse](docs/OpenChannelParticipantIdsResponse.md)
- [OpenChannelParticipantIdsResponseResult](docs/OpenChannelParticipantIdsResponseResult.md)
- [OpenChannelParticipantItem](docs/OpenChannelParticipantItem.md)
- [OpenChannelParticipantListByChannelRequest](docs/OpenChannelParticipantListByChannelRequest.md)
- [OpenChannelParticipantListRequest](docs/OpenChannelParticipantListRequest.md)
- [OpenChannelParticipantListResponse](docs/OpenChannelParticipantListResponse.md)
- [OpenChannelParticipantListResponseResult](docs/OpenChannelParticipantListResponseResult.md)
- [OpenChannelParticipantMuteListAddRequest](docs/OpenChannelParticipantMuteListAddRequest.md)
- [OpenChannelParticipantMuteListGetResponse](docs/OpenChannelParticipantMuteListGetResponse.md)
- [OpenChannelParticipantMuteListGetResponseResult](docs/OpenChannelParticipantMuteListGetResponseResult.md)
- [OpenChannelParticipantMuteListRemoveRequest](docs/OpenChannelParticipantMuteListRemoveRequest.md)
- [OpenChannelPriorityMessageTypeListRequest](docs/OpenChannelPriorityMessageTypeListRequest.md)
- [ProfanityWordBatchAddRequest](docs/ProfanityWordBatchAddRequest.md)
- [ProfanityWordBatchAddResponse](docs/ProfanityWordBatchAddResponse.md)
- [ProfanityWordBatchAddResponseResult](docs/ProfanityWordBatchAddResponseResult.md)
- [ProfanityWordBatchDeleteRequest](docs/ProfanityWordBatchDeleteRequest.md)
- [ProfanityWordDeleteRequest](docs/ProfanityWordDeleteRequest.md)
- [ProfanityWordItem](docs/ProfanityWordItem.md)
- [ProfanityWordListRequest](docs/ProfanityWordListRequest.md)
- [ProfanityWordListResponse](docs/ProfanityWordListResponse.md)
- [ProfanityWordListResponseResult](docs/ProfanityWordListResponseResult.md)
- [ProfanityWordListedItem](docs/ProfanityWordListedItem.md)
- [SingleMessageIdResponse](docs/SingleMessageIdResponse.md)
- [SingleMessageIdResponseResult](docs/SingleMessageIdResponseResult.md)
- [StreamMessageContent](docs/StreamMessageContent.md)
- [StreamMessageSendResponse](docs/StreamMessageSendResponse.md)
- [StreamMessageSendResponseResult](docs/StreamMessageSendResponseResult.md)
- [SystemChannelBroadcastAllRequest](docs/SystemChannelBroadcastAllRequest.md)
- [SystemChannelBroadcastDeleteRequest](docs/SystemChannelBroadcastDeleteRequest.md)
- [SystemChannelBroadcastOnlineRequest](docs/SystemChannelBroadcastOnlineRequest.md)
- [SystemChannelMessageSendRequest](docs/SystemChannelMessageSendRequest.md)
- [SystemChannelPushAudience](docs/SystemChannelPushAudience.md)
- [SystemChannelPushMessage](docs/SystemChannelPushMessage.md)
- [SystemChannelPushNotification](docs/SystemChannelPushNotification.md)
- [SystemChannelPushRequest](docs/SystemChannelPushRequest.md)
- [SystemChannelPushResponse](docs/SystemChannelPushResponse.md)
- [SystemChannelPushResponseResult](docs/SystemChannelPushResponseResult.md)
- [UserBanListRequest](docs/UserBanListRequest.md)
- [UserBanListResponse](docs/UserBanListResponse.md)
- [UserBanListResponseResult](docs/UserBanListResponseResult.md)
- [UserBanRequest](docs/UserBanRequest.md)
- [UserBlocklistAddRequest](docs/UserBlocklistAddRequest.md)
- [UserBlocklistGetRequest](docs/UserBlocklistGetRequest.md)
- [UserBlocklistGetResponse](docs/UserBlocklistGetResponse.md)
- [UserBlocklistGetResponseResult](docs/UserBlocklistGetResponseResult.md)
- [UserBlocklistRemoveRequest](docs/UserBlocklistRemoveRequest.md)
- [UserChannelTagAddRequest](docs/UserChannelTagAddRequest.md)
- [UserChannelTagItem](docs/UserChannelTagItem.md)
- [UserChannelTagListItem](docs/UserChannelTagListItem.md)
- [UserChannelTagListRequest](docs/UserChannelTagListRequest.md)
- [UserChannelTagListResponse](docs/UserChannelTagListResponse.md)
- [UserChannelTagListResponseResult](docs/UserChannelTagListResponseResult.md)
- [UserChannelTagRemoveRequest](docs/UserChannelTagRemoveRequest.md)
- [UserConnectionStatusRequest](docs/UserConnectionStatusRequest.md)
- [UserConnectionStatusResponse](docs/UserConnectionStatusResponse.md)
- [UserConnectionStatusResponseResult](docs/UserConnectionStatusResponseResult.md)
- [UserGetRequest](docs/UserGetRequest.md)
- [UserGetResponse](docs/UserGetResponse.md)
- [UserGetResult](docs/UserGetResult.md)
- [UserIdsMax100Request](docs/UserIdsMax100Request.md)
- [UserIdsMax20Request](docs/UserIdsMax20Request.md)
- [UserIdsRequest](docs/UserIdsRequest.md)
- [UserMessageSendResponse](docs/UserMessageSendResponse.md)
- [UserMessageSendResponseResult](docs/UserMessageSendResponseResult.md)
- [UserOperationResponse](docs/UserOperationResponse.md)
- [UserOperationResponseResult](docs/UserOperationResponseResult.md)
- [UserProfileBatchGetResponse](docs/UserProfileBatchGetResponse.md)
- [UserProfileBatchGetResponseResult](docs/UserProfileBatchGetResponseResult.md)
- [UserProfileItem](docs/UserProfileItem.md)
- [UserProfileListItem](docs/UserProfileListItem.md)
- [UserProfileListRequest](docs/UserProfileListRequest.md)
- [UserProfileListResponse](docs/UserProfileListResponse.md)
- [UserProfileListResponseResult](docs/UserProfileListResponseResult.md)
- [UserProfileSetRequest](docs/UserProfileSetRequest.md)
- [UserProfileSetResponse](docs/UserProfileSetResponse.md)
- [UserSoftDeletedListRequest](docs/UserSoftDeletedListRequest.md)
- [UserSoftDeletedListResponse](docs/UserSoftDeletedListResponse.md)
- [UserSoftDeletedListResponseResult](docs/UserSoftDeletedListResponseResult.md)
- [UserTagBatchGetItem](docs/UserTagBatchGetItem.md)
- [UserTagBatchGetRequest](docs/UserTagBatchGetRequest.md)
- [UserTagBatchGetResponse](docs/UserTagBatchGetResponse.md)
- [UserTagBatchGetResponseResult](docs/UserTagBatchGetResponseResult.md)
- [UserTagBatchSetRequest](docs/UserTagBatchSetRequest.md)
- [UserUpdateRequest](docs/UserUpdateRequest.md)


## Documentation For Authorization


Authentication schemes defined for the API:
### NexconnSignature

- **Type**: API key
- **API key parameter name**: App-Key
- **Location**: HTTP header


## Documentation for Utility Methods

Due to the fact that model structure members are all pointers, this package contains
a number of utility functions to easily obtain pointers to values of basic types.
Each of these functions takes a value of the given basic type and returns a pointer to it:

- `PtrBool`
- `PtrInt`
- `PtrInt32`
- `PtrInt64`
- `PtrFloat`
- `PtrFloat32`
- `PtrFloat64`
- `PtrString`
- `PtrTime`

## Package Info

- Repository: `https://github.com/NexconnAI-Dev/nexconn-server-sdk-go`
- Package version: `0.1.1`

## License

This project is licensed under the [MIT License](LICENSE).

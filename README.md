# ![LOGO](logo.png) Cloud Resource Manager **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Resource Manager API (version v2).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudresourcemanager/v2/swagger.json<br/>
Generated at: 2019-05-23T12:13:06+03:00

## API Description

Creates, reads, and updates metadata for Google Cloud Platform resource containers.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Gets the latest state of a long-running operation.  Clients can use this<br/>
> method to poll the operation result at intervals as recommended by the API<br/>
> service.

*Tags:* `operations`

#### Input Parameters
* `name` - _required_ - The name of the operation resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the Folders that are direct descendants of supplied parent resource.<br/>
> List provides a strongly consistent view of the Folders underneath<br/>
> the specified parent resource.<br/>
> List returns Folders sorted based upon the (ascending) lexical ordering<br/>
> of their display_name.<br/>
> The caller must have `resourcemanager.folders.list` permission on the<br/>
> identified parent.

*Tags:* `folders`

#### Input Parameters
* `pageSize` - _optional_ - The maximum number of Folders to return in the response.
This field is optional.
* `pageToken` - _optional_ - A pagination token returned from a previous call to `ListFolders`
that indicates where this listing should continue from.
This field is optional.
* `parent` - _optional_ - The resource name of the Organization or Folder whose Folders are
being listed.
Must be of the form `folders/{folder_id}` or `organizations/{org_id}`.
Access to this method is controlled by checking the
`resourcemanager.folders.list` permission on the `parent`.
* `showDeleted` - _optional_ - Controls whether Folders in the
DELETE_REQUESTED
state should be returned. Defaults to false. This field is optional.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a Folder in the resource hierarchy.<br/>
> Returns an Operation which can be used to track the progress of the<br/>
> folder creation workflow.<br/>
> Upon success the Operation.response field will be populated with the<br/>
> created Folder.<br/>
> <br/>
> In order to succeed, the addition of this new Folder must not violate<br/>
> the Folder naming, height or fanout constraints.<br/>
> <br/>
> + The Folder's display_name must be distinct from all other Folder's that<br/>
> share its parent.<br/>
> + The addition of the Folder must not cause the active Folder hierarchy<br/>
> to exceed a height of 4. Note, the full active + deleted Folder hierarchy<br/>
> is allowed to reach a height of 8; this provides additional headroom when<br/>
> moving folders that contain deleted folders.<br/>
> + The addition of the Folder must not cause the total number of Folders<br/>
> under its parent to exceed 100.<br/>
> <br/>
> If the operation fails due to a folder constraint violation, some errors<br/>
> may be returned by the CreateFolder request, with status code<br/>
> FAILED_PRECONDITION and an error description. Other folder constraint<br/>
> violations will be communicated in the Operation, with the specific<br/>
> PreconditionFailure returned via the details list in the Operation.error<br/>
> field.<br/>
> <br/>
> The caller must have `resourcemanager.folders.create` permission on the<br/>
> identified parent.

*Tags:* `folders`

#### Input Parameters
* `parent` - _optional_ - The resource name of the new Folder's parent.
Must be of the form `folders/{folder_id}` or `organizations/{org_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Search for folders that match specific filter criteria.<br/>
> Search provides an eventually consistent view of the folders a user has<br/>
> access to which meet the specified filter criteria.<br/>
> <br/>
> This will only return folders on which the caller has the<br/>
> permission `resourcemanager.folders.get`.

*Tags:* `folders`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Requests deletion of a Folder. The Folder is moved into the<br/>
> DELETE_REQUESTED state<br/>
> immediately, and is deleted approximately 30 days later. This method may<br/>
> only be called on an empty Folder in the<br/>
> ACTIVE state, where a Folder is empty if<br/>
> it doesn't contain any Folders or Projects in the<br/>
> ACTIVE state.<br/>
> The caller must have `resourcemanager.folders.delete` permission on the<br/>
> identified folder.

*Tags:* `folders`

#### Input Parameters
* `name` - _required_ - the resource name of the Folder to be deleted.
Must be of the form `folders/{folder_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Retrieves a Folder identified by the supplied resource name.<br/>
> Valid Folder resource names have the format `folders/{folder_id}`<br/>
> (for example, `folders/1234`).<br/>
> The caller must have `resourcemanager.folders.get` permission on the<br/>
> identified folder.

*Tags:* `folders`

#### Input Parameters
* `name` - _required_ - The resource name of the Folder to retrieve.
Must be of the form `folders/{folder_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a Folder, changing its display_name.<br/>
> Changes to the folder display_name will be rejected if they violate either<br/>
> the display_name formatting rules or naming constraints described in<br/>
> the CreateFolder documentation.<br/>
> <br/>
> The Folder's display name must start and end with a letter or digit,<br/>
> may contain letters, digits, spaces, hyphens and underscores and can be<br/>
> no longer than 30 characters. This is captured by the regular expression:<br/>
> [\p{L}\p{N}]([\p{L}\p{N}_- ]{0,28}[\p{L}\p{N}])?.<br/>
> The caller must have `resourcemanager.folders.update` permission on the<br/>
> identified folder.<br/>
> <br/>
> If the update fails due to the unique name constraint then a<br/>
> PreconditionFailure explaining this violation will be returned<br/>
> in the Status.details field.

*Tags:* `folders`

#### Input Parameters
* `name` - _required_ - Output only. The resource name of the Folder.
Its format is `folders/{folder_id}`, for example: "folders/1234".
* `updateMask` - _optional_ - Fields to be updated.
Only the `display_name` can be updated.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Moves a Folder under a new resource parent.<br/>
> Returns an Operation which can be used to track the progress of the<br/>
> folder move workflow.<br/>
> Upon success the Operation.response field will be populated with the<br/>
> moved Folder.<br/>
> Upon failure, a FolderOperationError categorizing the failure cause will<br/>
> be returned - if the failure occurs synchronously then the<br/>
> FolderOperationError will be returned via the Status.details field<br/>
> and if it occurs asynchronously then the FolderOperation will be returned<br/>
> via the Operation.error field.<br/>
> In addition, the Operation.metadata field will be populated with a<br/>
> FolderOperation message as an aid to stateless clients.<br/>
> Folder moves will be rejected if they violate either the naming, height<br/>
> or fanout constraints described in the<br/>
> CreateFolder documentation.<br/>
> The caller must have `resourcemanager.folders.move` permission on the<br/>
> folder's current and proposed new parent.

*Tags:* `folders`

#### Input Parameters
* `name` - _required_ - The resource name of the Folder to move.
Must be of the form folders/{folder_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Cancels the deletion request for a Folder. This method may only be<br/>
> called on a Folder in the<br/>
> DELETE_REQUESTED state.<br/>
> In order to succeed, the Folder's parent must be in the<br/>
> ACTIVE state.<br/>
> In addition, reintroducing the folder into the tree must not violate<br/>
> folder naming, height and fanout constraints described in the<br/>
> CreateFolder documentation.<br/>
> The caller must have `resourcemanager.folders.undelete` permission on the<br/>
> identified folder.

*Tags:* `folders`

#### Input Parameters
* `name` - _required_ - The resource name of the Folder to undelete.
Must be of the form `folders/{folder_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the access control policy for a Folder. The returned policy may be<br/>
> empty if no such policy or resource exists. The `resource` field should<br/>
> be the Folder's resource name, e.g. "folders/1234".<br/>
> The caller must have `resourcemanager.folders.getIamPolicy` permission<br/>
> on the identified folder.

*Tags:* `folders`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets the access control policy on a Folder, replacing any existing policy.<br/>
> The `resource` field should be the Folder's resource name, e.g.<br/>
> "folders/1234".<br/>
> The caller must have `resourcemanager.folders.setIamPolicy` permission<br/>
> on the identified folder.

*Tags:* `folders`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being specified.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns permissions that a caller has on the specified Folder.<br/>
> The `resource` field should be the Folder's resource name,<br/>
> e.g. "folders/1234".<br/>
> <br/>
> There are no permissions required for making this API call.

*Tags:* `folders`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy detail is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudresourcemanager-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

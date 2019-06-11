# ![LOGO](logo.png) ApiManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ApiManagementClient API (version 2018-06-01-preview).

Generated from: https://api.apis.guru/v2/specs/azure.com/apimanagement-apimgroups/2018-06-01-preview/swagger.json<br/>
Generated at: 2019-06-11T18:13:13+03:00

## API Description

Use these REST APIs for performing operations on Group entity in your Azure API Management deployment. Groups are used to manage the visibility of products to developers. Each API Management service instance comes with the following immutable system groups whose membership is automatically managed by API Management.  - **Administrators** - Azure subscription administrators are members of this group. - **Developers** - Authenticated developer portal users fall into this group. - **Guests** - Unauthenticated developer portal users are placed into this group. In addition to these system groups, administrators can create custom groups or [leverage external groups in associated Azure Active Directory tenants](https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-aad#how-to-add-an-external-azure-active-directory-group). Custom and external groups can be used alongside system groups in giving developers visibility and access to API products. For example, you could create one custom group for developers affiliated with a specific partner organization and allow them access to the APIs from a product containing relevant APIs only. A user can be a member of more than one group.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists a collection of groups defined within a service instance.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|displayName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|description | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|aadObjectId | eq |    |

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes specific group of the API Management service instance.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the group specified by its identifier.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the entity state (Etag) version of the group specified by its identifier.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the details of the group specified by its identifier.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - ETag of the Entity. ETag should match the current entity state from the header response of the GET request or it should be * for unconditional update.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or Updates a group.

*Tags:* `Group`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - ETag of the Entity. Not required when creating an entity, but required when updating an entity.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists a collection of user entities associated with the group.

*Tags:* `GroupUser`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions               |
|-------------|------------------------|-----------------------------------|

|name | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|firstName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|lastName | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|email | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|
|registrationDate | ge, le, eq, ne, gt, lt |    |
|note | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith|

* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Remove existing user from existing group.

*Tags:* `GroupUser`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `userId` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Checks that user entity specified by identifier is associated with the group entity.

*Tags:* `GroupUser`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `userId` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Add existing user to existing group

*Tags:* `GroupUser`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `groupId` - _required_ - Group identifier. Must be unique in the current API Management service instance.
* `userId` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-apimanagement-apimgroups-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

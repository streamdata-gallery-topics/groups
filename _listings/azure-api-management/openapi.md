swagger: "2.0"
x-collection-name: Azure API Management
x-complete: 1
info:
  title: ApiManagementClient
  description: use-these-rest-apis-for-performing-operations-on-user-entity-in-azure-api-management-deployment--the-user-entity-in-api-management-represents-the-developers-that-call-the-apis-of-the-products-to-which-they-are-subscribed-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}/groups
  : get:
      summary: Groups ListByService
      description: Lists a collection of groups defined within a service instance.
      operationId: Groups_ListByService
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenamegroups-get
      parameters:
      - in: query
        name: $filter
        description: '| Field       | Supported operators    | Supported functions                         ||-------------|------------------------|---------------------------------------------||
          id          | ge, le, eq, ne, gt, lt | substringof, contains, startswith,
          endswith || name        | ge, le, eq, ne, gt, lt | substringof, contains,
          startswith, endswith || description | ge, le, eq, ne, gt, lt | substringof,
          contains, startswith, endswith || type        | eq, ne                 |
          N/A                                         |'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}/groups/{groupId}
  : get:
      summary: Groups Get
      description: Gets the details of the group specified by its identifier.
      operationId: Groups_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenamegroupsgroupid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
    put:
      summary: Groups CreateOrUpdate
      description: Creates or Updates a group.
      operationId: Groups_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenamegroupsgroupid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Create parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Groups
    patch:
      summary: Groups Update
      description: Updates the details of the group specified by its identifier.
      operationId: Groups_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenamegroupsgroupid-patch
      parameters:
      - in: header
        name: If-Match
        description: ETag of the Group Entity
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Update parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Groups
    delete:
      summary: Groups Delete
      description: Deletes specific group of the API Management service instance.
      operationId: Groups_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenamegroupsgroupid-delete
      parameters:
      - in: header
        name: If-Match
        description: ETag of the Group Entity
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
---
swagger: "2.0"
x-collection-name: Azure Resource Manager
x-complete: 0
info:
  title: Azure Resource Manager API Resource Groups List
  description: Gets all the resource groups for a subscription.
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
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/resources:
    get:
      summary: Resource Groups List Resources
      description: Get all the resources for a resource group.
      operationId: ResourceGroups_ListResources
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameresources-get
      parameters:
      - in: query
        name: $expand
        description: The $expand query parameter
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: query
        name: $top
        description: The number of results to return
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group with the resources to get
      responses:
        200:
          description: OK
      tags:
      - Resource Groups
  /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}:
    head:
      summary: Resource Groups Check Existence
      description: Checks whether a resource group exists.
      operationId: ResourceGroups_CheckExistence
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupname-head
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group to check
      responses:
        200:
          description: OK
      tags:
      - Resource Groups Existence
    put:
      summary: Resource Groups Create Or Update
      description: Creates a resource group.
      operationId: ResourceGroups_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupname-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to the create or update a resource group
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group to create or update
      responses:
        200:
          description: OK
      tags:
      - Resource Groups
    get:
      summary: Resource Groups Get
      description: Gets a resource group.
      operationId: ResourceGroups_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupname-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group to get
      responses:
        200:
          description: OK
      tags:
      - Resource Groups
  /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}/exportTemplate:
    post:
      summary: Resource Groups Export Template
      description: Captures the specified resource group as a template.
      operationId: ResourceGroups_ExportTemplate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameexporttemplate-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters for exporting the template
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group to export as a template
      responses:
        200:
          description: OK
      tags:
      - Resource Groups Export Template
  /subscriptions/{subscriptionId}/resourcegroups:
    get:
      summary: Resource Groups List
      description: Gets all the resource groups for a subscription.
      operationId: ResourceGroups_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroups-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: query
        name: $top
        description: The number of results to return
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Resource Groups
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
swagger: "2.0"
x-collection-name: Apica
x-complete: 1
info:
  title: Scenarios API
  version: 1.0.0
host: api.pingdom.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
basePath: /
paths:
  '/groups ':
    ' get ':
      summary: Groups
      description: Gets a hierarchy of all monitor groups that are visible to you
        as a user or a customer depending on the request context.
      operationId: -groups-
      x-api-path-slug: groups-get
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' post ':
      summary: Groups
      description: Creates a new monitor group.
      operationId: -groups-
      x-api-path-slug: groups-post
      responses:
        200:
          description: OK
      tags:
      - Groups
  '/groups/{groupId} ':
    ' put ':
      summary: Groups
      description: Updates a monitor group.
      operationId: -groups-groupid-
      x-api-path-slug: groupsgroupid-put
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' delete ':
      summary: Groups
      description: Deletes a monitor group by Id.
      operationId: -groups-groupid-
      x-api-path-slug: groupsgroupid-delete
      responses:
        200:
          description: OK
      tags:
      - Groups
  '/groups/{groupId}/checks ':
    ' get ':
      summary: Group Checks
      description: Gets a list of checks assigned to the monitor group.
      operationId: -groups-groupid-checks-
      x-api-path-slug: groupsgroupidchecks-get
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' post ':
      summary: Group Checks
      description: Assigns checks to the monitor group.
      operationId: -groups-groupid-checks-
      x-api-path-slug: groupsgroupidchecks-post
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' delete ':
      summary: Groups Checks
      description: Unassigns checks from the monitor group.
      operationId: -groups-groupid-checks-
      x-api-path-slug: groupsgroupidchecks-delete
      responses:
        200:
          description: OK
      tags:
      - Groups
  '/groups/{groupId}/users ':
    ' get ':
      summary: Groups Users
      description: Gets a list of users assigned to the monitor group.
      operationId: -groups-groupid-users-
      x-api-path-slug: groupsgroupidusers-get
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' post ':
      summary: Groups Users
      description: Assigns users to the monitor group.
      operationId: -groups-groupid-users-
      x-api-path-slug: groupsgroupidusers-post
      responses:
        200:
          description: OK
      tags:
      - Groups
    ' delete ':
      summary: Groups Users
      description: ""
      operationId: -groups-groupid-users-
      x-api-path-slug: groupsgroupidusers-delete
      responses:
        200:
          description: OK
      tags:
      - Groups
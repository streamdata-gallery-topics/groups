---
swagger: "2.0"
x-collection-name: Learnifier
x-complete: 0
info:
  title: Learnifier List of all users in group.
  version: 1.1.0
  description: Returns a list of all members in User Groups that are based on the
    Global Group with this groupid.
host: learnifier.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /globalusergroups:
    get:
      summary: List Global User Groups.
      description: Returns a list of Global User Groups. Global User Groups are set
        up for the realm, and will generate groups that can be used on the client
        level.
      operationId: globalusergroups.get
      x-api-path-slug: globalusergroups-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - Groups
  /globalusergroups/{groupid}/members:
    get:
      summary: List of all users in group.
      description: Returns a list of all members in User Groups that are based on
        the Global Group with this groupid.
      operationId: globalusergroups.groupid.members.get
      x-api-path-slug: globalusergroupsgroupidmembers-get
      parameters:
      - in: path
        name: groupid
        description: ID of group
      responses:
        200:
          description: OK
      tags:
      - Users
      - Groups
  /orgunits/{orgid}/usergroups:
    get:
      summary: List User Groups.
      description: Returns a list of User Groups for the org unit.
      operationId: orgunits.orgid.usergroups.get
      x-api-path-slug: orgunitsorgidusergroups-get
      parameters:
      - in: path
        name: orgid
        description: ID of organization
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Users
      - Groups
    post:
      summary: Create a User Group.
      description: Create a User Group.
      operationId: orgunits.orgid.usergroups.post
      x-api-path-slug: orgunitsorgidusergroups-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orgid
        description: ID of organization
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Users
      - Groups
  /orgunits/{orgid}/usergroups/{groupid}:
    get:
      summary: Get user group
      description: Returns single User Group.
      operationId: orgunits.orgid.usergroups.groupid.get
      x-api-path-slug: orgunitsorgidusergroupsgroupid-get
      parameters:
      - in: path
        name: groupid
        description: ID of group
      - in: path
        name: orgid
        description: ID of organization
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Users
      - Groups
      - Groupid
  /orgunits/{orgid}/usergroups/{groupid}/members:
    get:
      summary: List of all users in group.
      description: Returns a list of all members in User Groups that are based on
        the Global Group with this groupid.
      operationId: orgunits.orgid.usergroups.groupid.members.get
      x-api-path-slug: orgunitsorgidusergroupsgroupidmembers-get
      parameters:
      - in: path
        name: groupid
        description: ID of group
      - in: path
        name: orgid
        description: ID of organization
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Uses
      - Groups
      - Members
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
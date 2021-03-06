---
swagger: "2.0"
x-collection-name: CollabNet
x-complete: 0
info:
  title: CollabNet TeamForge API Documentation Removes project group admin
  version: 1.0.0
  description: Removes project group admin.
basePath: /ctfrest/foundation/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{userid}/groups/{groupid}:
    put:
      summary: Add user to a user group by user id
      description: Add user to a user group by user id.
      operationId: addUserToGroupByUserid
      x-api-path-slug: usersuseridgroupsgroupid-put
      parameters:
      - in: path
        name: groupid
        description: Group id
      - in: path
        name: userid
        description: User id
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - User
      - Group
      - By
      - User
  /users/{userid}/groups:
    get:
      summary: Gets a user's group list by user id
      description: Gets a user's group list by user id.
      operationId: getUserGroupsByUserid
      x-api-path-slug: usersuseridgroups-get
      parameters:
      - in: path
        name: userid
        description: User id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Group
      - List
      - By
      - User
  /users/myself/groups/{groupid}:
    put:
      summary: Add current user to a user group
      description: Add current user to a user group.
      operationId: addMyselfToGroup
      x-api-path-slug: usersmyselfgroupsgroupid-put
      parameters:
      - in: path
        name: groupid
        description: Group id
      responses:
        200:
          description: OK
      tags:
      - Current
      - User
      - To
      - User
      - Group
  /users/myself/groups:
    get:
      summary: Gets current user's group list
      description: Gets current user's group list.
      operationId: getMyUserGroups
      x-api-path-slug: usersmyselfgroups-get
      responses:
        200:
          description: OK
      tags:
      - Current
      - Users
      - Group
      - List
  /users/by-username/{username}/groups/{groupid}:
    put:
      summary: Add user to a user group by user name
      description: Add user to a user group by user name.
      operationId: addUserToGroupByUsername
      x-api-path-slug: usersbyusernameusernamegroupsgroupid-put
      parameters:
      - in: path
        name: groupid
        description: Group id
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - User
      - Group
      - By
      - User
      - Name
  /users/by-username/{username}/groups:
    get:
      summary: Gets a user's group list by username
      description: Gets a user's group list by username.
      operationId: getUserGroupsByUsername
      x-api-path-slug: usersbyusernameusernamegroups-get
      parameters:
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Users
      - Group
      - List
      - By
      - Username
  /projectgroups/{projectgroupid}/projects/{projectid}:
    delete:
      summary: Removes project from group
      description: Removes project from group.
      operationId: removeProjectFromGroup
      x-api-path-slug: projectgroupsprojectgroupidprojectsprojectid-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - From
      - Group
    put:
      summary: Adds project to project group
      description: Adds project to project group.
      operationId: addProjectToGroup
      x-api-path-slug: projectgroupsprojectgroupidprojectsprojectid-put
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - To
      - Project
      - Group
  /projectgroups/{projectgroupid}/projects:
    get:
      summary: Gets project group projects
      description: Gets project group projects.
      operationId: getProjectGroupProjects
      x-api-path-slug: projectgroupsprojectgroupidprojects-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Projects
  /projectgroups/{projectgroupid}/members/{username}:
    delete:
      summary: Removes project group member
      description: Removes project group member.
      operationId: removeProjectGroupMember
      x-api-path-slug: projectgroupsprojectgroupidmembersusername-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - Group
      - Member
    put:
      summary: Adds project group member
      description: Adds project group member.
      operationId: addProjectGroupMember
      x-api-path-slug: projectgroupsprojectgroupidmembersusername-put
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Member
  /projectgroups/{projectgroupid}/members:
    get:
      summary: Gets project group members
      description: Gets project group members.
      operationId: getProjectGroupMembers
      x-api-path-slug: projectgroupsprojectgroupidmembers-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Members
  /projectgroups/{projectgroupid}/admins/{username}:
    delete:
      summary: Removes project group admin
      description: Removes project group admin.
      operationId: removeProjectGroupAdmin
      x-api-path-slug: projectgroupsprojectgroupidadminsusername-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - Group
      - Admin
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
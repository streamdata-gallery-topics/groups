---
swagger: "2.0"
info:
  title: Amazon RDS API Create D B Parameter Group
  version: 1.0.0
  description: Creates a new DB parameter group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateDBParameterGroup:
    get:
      summary: Create D B Parameter Group
      description: Creates a new DB parameter group
      operationId: createdbparametergroup
      parameters:
      - in: query
        name: DBParameterGroupFamily
        description: The DB parameter group family name
        type: string
      - in: query
        name: DBParameterGroupName
        description: The name of the DB parameter group
        type: string
      - in: query
        name: Description
        description: The description for the DB parameter group
        type: string
      - in: query
        name: Tags.Tag.N
        description: A list of tags
        type: string
      responses:
        200:
          description: OK
      tags:
      - parameter groups
definitions: []
x-collection-name: AWS RDS
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
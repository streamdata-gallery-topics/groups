---
swagger: "2.0"
info:
  title: Amazon RDS API Modify D B Parameter Group
  version: 1.0.0
  description: Modifies the parameters of a DB parameter group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ModifyDBParameterGroup:
    get:
      summary: Modify D B Parameter Group
      description: Modifies the parameters of a DB parameter group
      operationId: modifydbparametergroup
      parameters:
      - in: query
        name: DBParameterGroupName
        description: The name of the DB parameter group
        type: string
      - in: query
        name: Parameters.Parameter.N
        description: An array of parameter names, values, and the apply method for
          the parameter update
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
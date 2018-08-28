---
swagger: "2.0"
x-collection-name: PayRun
x-complete: 0
info:
  title: Pay Run.IO Updates a transform definition
  description: Updates the existing specified transform definition object
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Transform/{TransformDefinitionId}:
    delete:
      summary: Deletes a transform definition
      description: Delete the specified transform definition
      operationId: DeleteTransformDefinition
      x-api-path-slug: transformtransformdefinitionid-delete
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: TransformDefinitionId
        description: The transform definition unique identifier
      responses:
        200:
          description: OK
      tags:
      - Transform
      - Definition
    get:
      summary: Get the transform definition
      description: Returns the specified transform definition from the authroised
        application
      operationId: GetTransformDefinitionFromApplication
      x-api-path-slug: transformtransformdefinitionid-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: TransformDefinitionId
        description: The transform definition unique identifier
      responses:
        200:
          description: OK
      tags:
      - Transform
      - Definition
    put:
      summary: Updates a transform definition
      description: Updates the existing specified transform definition object
      operationId: PutTransformDefinition
      x-api-path-slug: transformtransformdefinitionid-put
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: body
        name: TransformDefinition
        description: The transform definition object to be executed against the report
          data
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: TransformDefinitionId
        description: The transform definition unique identifier
      responses:
        200:
          description: OK
      tags:
      - Transform
      - Definition
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
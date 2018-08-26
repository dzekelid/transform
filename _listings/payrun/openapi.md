---
swagger: "2.0"
x-collection-name: PayRun
x-complete: 1
info:
  title: Pay Run.IO
  description: open-scableable-transparent-payroll-api-
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
  /Transforms:
    get:
      summary: Gets all transform definitions
      description: Get links to all saved transform definitions under authorised application
      operationId: GetTransformDefinitionsFromApplication
      x-api-path-slug: transforms-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - ""
      - Transform
      - Definitions
    post:
      summary: Create a new transform definition
      description: Creates a new transform defintion object
      operationId: PostTransformDefinition
      x-api-path-slug: transforms-post
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
      responses:
        200:
          description: OK
      tags:
      - New
      - Transform
      - Definition
---
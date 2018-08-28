---
swagger: "2.0"
x-collection-name: AWS WorkSpaces
x-complete: 0
info:
  title: AWS WorkSpaces Service API Create Tags
  version: 1.0.0
  description: Creates tags for a WorkSpace.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateTags:
    get:
      summary: Create Tags
      description: Creates tags for a WorkSpace.
      operationId: createTags
      x-api-path-slug: actioncreatetags-get
      parameters:
      - in: query
        name: ResourceId
        description: The resource ID of the request
        type: string
      - in: query
        name: Tags
        description: The tags of the request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tags
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
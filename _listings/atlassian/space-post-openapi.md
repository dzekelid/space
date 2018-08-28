---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Create space
  description: |-
    Creates a new space. Note, currently you cannot set space labels when
    creating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Create Space(s)' global permission.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /space:
    post:
      summary: Create space
      description: |-
        Creates a new space. Note, currently you cannot set space labels when
        creating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Create Space(s)' global permission.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createSpace_post
      x-api-path-slug: space-post
      responses:
        200:
          description: OK
      tags:
      - Space
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
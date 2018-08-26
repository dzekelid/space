---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Create space property
  description: "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
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
  /space/_private:
    post:
      summary: Create private space
      description: |-
        Creates a new space that is only visible to the creator. This method is
        the same as the [Create space](#api-space-post) method with permissions
        set to the current user only. Note, currently you cannot set space
        labels when creating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Create Space(s)' global permission.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createPrivateSpace_post
      x-api-path-slug: space-private-post
      responses:
        200:
          description: OK
      tags:
      - Private
      - Space
  /space/{spaceKey}:
    get:
      summary: Get space
      description: |-
        Returns a space. This includes information like the name, description,
        and permissions, but not the content in the space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpace_get
      x-api-path-slug: spacespacekey-get
      parameters:
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the space
          toexpand, where:  - `settings` returns the settings for the space, similar
          to [Get space settings](#api-space-spaceKey-settings-get)'
      - in: path
        name: spaceKey
        description: The key of the space to be returned
      responses:
        200:
          description: OK
      tags:
      - Space
    put:
      summary: Update space
      description: |-
        Updates the name, description, or homepage of a space.

        -   For security reasons, permissions cannot be updated via the API and
        must be changed via the user interface instead.
        -   Currently you cannot set space labels when updating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpace_put
      x-api-path-slug: spacespacekey-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to update
      responses:
        200:
          description: OK
      tags:
      - Space
    delete:
      summary: Delete space
      description: |-
        Deletes a space. Note, the space will be deleted in a long running task.
        Therefore, the space may not be deleted yet when this method has
        returned. Clients should poll the status link that is returned in the
        response until the task completes.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.deleteSpace_delete
      x-api-path-slug: spacespacekey-delete
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to delete
      responses:
        200:
          description: OK
      tags:
      - Space
  /space/{spaceKey}/property:
    get:
      summary: Get space properties
      description: "Returns all properties for the given space. Space properties are
        a key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperties_get
      x-api-path-slug: spacespacekeyproperty-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the spaceproperty
          to expand
      - in: query
        name: limit
        description: The maximum number of properties to return per page
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its properties
      - in: query
        name: start
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Space
      - Properties
    post:
      summary: Create space property
      description: "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpaceProperty_post
      x-api-path-slug: spacespacekeyproperty-post
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space that the property will be created in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
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
---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Remove space watch
  description: "Removes a user as a watcher from a space. Choose the user by doing
    one of \nthe following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
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
  /space/{spaceKey}/property/{key}:
    get:
      summary: Get space property
      description: "Returns a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperty_get
      x-api-path-slug: spacespacekeypropertykey-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the spaceproperty
          to expand
      - in: path
        name: key
        description: The key of the space property
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
    post:
      summary: Create space property for key
      description: "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property`
        but the key for the property is passed as a\npath parameter, rather than in
        the request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpacePropertyForKey_p
      x-api-path-slug: spacespacekeypropertykey-post
      parameters:
      - in: path
        name: key
        description: The key of the property to be created
      - in: path
        name: spaceKey
        description: The key of the space that the property will be created in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Propertykey
    put:
      summary: Update space property
      description: "Updates a space property. Note, you cannot update the key of a
        space\nproperty, only the value.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.updateSpaceProperty_put
      x-api-path-slug: spacespacekeypropertykey-put
      parameters:
      - in: path
        name: key
        description: The key of the property to be updated
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
    delete:
      summary: Delete space property
      description: "Deletes a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.deleteSpaceProperty_delete
      x-api-path-slug: spacespacekeypropertykey-delete
      parameters:
      - in: path
        name: key
        description: The key of the property to be deleted
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
  /space/{spaceKey}/settings:
    get:
      summary: Get space settings
      description: |-
        Returns the settings of a space. Currently only the
        `routeOverrideEnabled` setting can be returned.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaceSettings_get
      x-api-path-slug: spacespacekeysettings-get
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its settings
      responses:
        200:
          description: OK
      tags:
      - Space
      - Settings
    put:
      summary: Update space settings
      description: |-
        Updates the settings for a space. Currently only the
        `routeOverrideEnabled` setting can be updated.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpaceSettings_put
      x-api-path-slug: spacespacekeysettings-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space whose settings will be updated
      responses:
        200:
          description: OK
      tags:
      - Space
      - Settings
  /space/{spaceKey}/theme:
    get:
      summary: Get space theme
      description: "Returns the theme selected for a space, if one is set. If no space
        \ntheme is set, this means that the space is inheriting the global look \nand
        feel settings.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.getSpaceTheme_get
      x-api-path-slug: spacespacekeytheme-get
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its theme
      responses:
        200:
          description: OK
      tags:
      - Space
      - Theme
    put:
      summary: Set space theme
      description: "Sets the theme for a space. Note, if you want to reset the space
        theme to \nthe default Confluence theme, use the 'Reset space theme' method
        instead \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.setSpaceTheme_put
      x-api-path-slug: spacespacekeytheme-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to set the theme for
      responses:
        200:
          description: OK
      tags:
      - Set
      - Space
      - Theme
    delete:
      summary: Reset space theme
      description: "Resets the space theme. This means that the space will inherit
        the \nglobal look and feel settings\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.resetSpaceTheme_delete
      x-api-path-slug: spacespacekeytheme-delete
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to reset the theme for
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Space
      - Theme
  /user/watch/space/{spaceKey}:
    get:
      summary: Get space watch status
      description: "Returns whether a user is watching a space. Choose the user by
        \ndoing one of the following:\n\n- Specify a user via a query parameter: Use
        the `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.isWatchingSpace_get
      x-api-path-slug: userwatchspacespacekey-get
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user to be queried for whether they are
          watching the space
      - in: query
        name: key
        description: The `key` of the user to be queried for whether they are watching
          the space
      - in: path
        name: spaceKey
        description: The key of the space to be queried for whether the specified
          user is watching it
      - in: query
        name: username
        description: The `username` of the user to be queried for whether they are
          watching the space
      responses:
        200:
          description: OK
      tags:
      - Space
      - Watch
      - Status
    post:
      summary: Add space watcher
      description: "Adds a user as a watcher to a space. Choose the user by doing
        one of the \nfollowing:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token:
        no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addSpaceWatcher_post
      x-api-path-slug: userwatchspacespacekey-post
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be added as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be added as a watcher
      - in: path
        name: spaceKey
        description: The key of the space to add the watcher to
      - in: query
        name: username
        description: The `username` of the user that will be added as a watcher
      responses:
        200:
          description: OK
      tags:
      - Space
      - Watcher
    delete:
      summary: Remove space watch
      description: "Removes a user as a watcher from a space. Choose the user by doing
        one of \nthe following:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.removeSpaceWatch_delete
      x-api-path-slug: userwatchspacespacekey-delete
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be removed as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be removed as a watcher
      - in: path
        name: spaceKey
        description: The key of the space to remove the watcher from
      - in: query
        name: username
        description: The `username` of the user that will be removed as a watcher
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Space
      - Watch
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
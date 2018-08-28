---
name: Atlassian
x-slug: atlassian
description: Millions of users globally rely on Atlassian products every day for improving
  software development, project management, collaboration, and code quality.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
x-kinRank: "8"
x-alexaRank: "1656"
tags: Space
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/apis.md
specificationVersion: "0.14"
apis:
- name: The Confluence Cloud REST API - Create space
  x-api-slug: space-post
  description: |-
    Creates a new space. Note, currently you cannot set space labels when
    creating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Create Space(s)' global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/space-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/space-post-openapi.md
- name: The Confluence Cloud REST API - Create private space
  x-api-slug: space-private-post
  description: |-
    Creates a new space that is only visible to the creator. This method is
    the same as the [Create space](#api-space-post) method with permissions
    set to the current user only. Note, currently you cannot set space
    labels when creating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Create Space(s)' global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/space-private-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/space-private-post-openapi.md
- name: The Confluence Cloud REST API - Get space
  x-api-slug: spacespacekey-get
  description: |-
    Returns a space. This includes information like the name, description,
    and permissions, but not the content in the space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-get-openapi.md
- name: The Confluence Cloud REST API - Update space
  x-api-slug: spacespacekey-put
  description: |-
    Updates the name, description, or homepage of a space.

    -   For security reasons, permissions cannot be updated via the API and
    must be changed via the user interface instead.
    -   Currently you cannot set space labels when updating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-put-openapi.md
- name: The Confluence Cloud REST API - Delete space
  x-api-slug: spacespacekey-delete
  description: |-
    Deletes a space. Note, the space will be deleted in a long running task.
    Therefore, the space may not be deleted yet when this method has
    returned. Clients should poll the status link that is returned in the
    response until the task completes.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekey-delete-openapi.md
- name: The Confluence Cloud REST API - Get space properties
  x-api-slug: spacespacekeyproperty-get
  description: "Returns all properties for the given space. Space properties are a
    key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeyproperty-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeyproperty-get-openapi.md
- name: The Confluence Cloud REST API - Create space property
  x-api-slug: spacespacekeyproperty-post
  description: "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeyproperty-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeyproperty-post-openapi.md
- name: The Confluence Cloud REST API - Get space property
  x-api-slug: spacespacekeypropertykey-get
  description: "Returns a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-get-openapi.md
- name: The Confluence Cloud REST API - Create space property for key
  x-api-slug: spacespacekeypropertykey-post
  description: "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property`
    but the key for the property is passed as a\npath parameter, rather than in the
    request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-post-openapi.md
- name: The Confluence Cloud REST API - Update space property
  x-api-slug: spacespacekeypropertykey-put
  description: "Updates a space property. Note, you cannot update the key of a space\nproperty,
    only the value.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-put-openapi.md
- name: The Confluence Cloud REST API - Delete space property
  x-api-slug: spacespacekeypropertykey-delete
  description: "Deletes a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeypropertykey-delete-openapi.md
- name: The Confluence Cloud REST API - Get space settings
  x-api-slug: spacespacekeysettings-get
  description: |-
    Returns the settings of a space. Currently only the
    `routeOverrideEnabled` setting can be returned.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeysettings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeysettings-get-openapi.md
- name: The Confluence Cloud REST API - Update space settings
  x-api-slug: spacespacekeysettings-put
  description: |-
    Updates the settings for a space. Currently only the
    `routeOverrideEnabled` setting can be updated.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeysettings-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeysettings-put-openapi.md
- name: The Confluence Cloud REST API - Get space theme
  x-api-slug: spacespacekeytheme-get
  description: "Returns the theme selected for a space, if one is set. If no space
    \ntheme is set, this means that the space is inheriting the global look \nand
    feel settings.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-get-openapi.md
- name: The Confluence Cloud REST API - Set space theme
  x-api-slug: spacespacekeytheme-put
  description: "Sets the theme for a space. Note, if you want to reset the space theme
    to \nthe default Confluence theme, use the 'Reset space theme' method instead
    \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-put-openapi.md
- name: The Confluence Cloud REST API - Reset space theme
  x-api-slug: spacespacekeytheme-delete
  description: "Resets the space theme. This means that the space will inherit the
    \nglobal look and feel settings\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/spacespacekeytheme-delete-openapi.md
- name: The Confluence Cloud REST API - Get space watch status
  x-api-slug: userwatchspacespacekey-get
  description: "Returns whether a user is watching a space. Choose the user by \ndoing
    one of the following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-get-openapi.md
- name: The Confluence Cloud REST API - Add space watcher
  x-api-slug: userwatchspacespacekey-post
  description: "Adds a user as a watcher to a space. Choose the user by doing one
    of the \nfollowing:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header
    when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-post-openapi.md
- name: The Confluence Cloud REST API - Remove space watch
  x-api-slug: userwatchspacespacekey-delete
  description: "Removes a user as a watcher from a space. Choose the user by doing
    one of \nthe following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/space/master/_listings/atlassian/userwatchspacespacekey-delete-openapi.md
x-common:
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/confluence/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/software/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/service-desk/swagger.v3.json
- type: x-website
  url: http://atlassian.com/
- type: x-website
  url: http://www.atlassian.com
- type: x-api-gallery
  url: http://att.dev.program.api.gallery.streamdata.io
- type: x-api-stack
  url: http://atlassian.stack.network
- type: x-blog
  url: http://blogs.atlassian.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/atlassian
- type: x-crunchbase
  url: http://www.crunchbase.com/company/atlassian
- type: x-email
  url: copyright@atlassian.com
- type: x-email
  url: trademarks@atlassian.com
- type: x-email
  url: sales@atlassian.com
- type: x-email
  url: ar_enterprise@atlassian.com
- type: x-email
  url: privacy@atlassian.com
- type: x-email
  url: eudatarep@atlassian.com
- type: x-email
  url: experts@atlassian.com
- type: x-email
  url: remittance@atlassian.com
- type: x-email
  url: ap@atlassian.com
- type: x-email
  url: procurement@atlassian.com
- type: x-github
  url: https://github.com/atlassian
- type: x-privacy-policy
  url: https://www.atlassian.com/legal/privacy-policy?_ga=2.188884514.868776184.1519225620-845241124.1519225620
- type: x-twitter
  url: https://twitter.com/atlassian
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
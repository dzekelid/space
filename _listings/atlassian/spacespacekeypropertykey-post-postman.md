{
  "info": {
    "name": "Confluence Cloud API Create space property for key",
    "_postman_id": "2e4ac8f5-f542-48a0-8b06-a54e249d8ec8",
    "description": "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property` but the key for the property is passed as a\npath parameter, rather than in the request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n‘Admin’ permission for the space.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "121fff07-3736-4df0-9698-840e62649853",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecords_get",
          "request": {
            "url": "{{default}}/audit?endDate=%7B%7D&limit=%7B%7D&searchString=%7B%7D&start=%7B%7D&startDate=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all records in the audit log, optionally for a certain date range. \nThis contains information about events like space exports, group membership \nchanges, app installations, etc. For more information, see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html) \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "711aee5b-bd26-4d49-a03f-77c708ce8026"
            }
          ]
        },
        {
          "id": "7d9254b0-27b3-4386-9ce5-9f7dc6ec6246",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.createAuditRecord_post",
          "request": {
            "url": "{{default}}/audit",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a record in the audit log. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "857d3d8c-dc94-4c7a-b172-150d0407333e"
            }
          ]
        },
        {
          "id": "21332585-7633-458a-8b24-aa7fbd41ed7a",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecordsForTimePeriod_get",
          "request": {
            "url": "{{default}}/audit/since?limit=%7B%7D&number=%7B%7D&searchString=%7B%7D&start=%7B%7D&units=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns records from the audit log, for a time period back from the current \ndate. For example, you can use this method to get the last 3 months of records.\n\nThis contains information about events like space exports, group membership \nchanges, app installations, etc. For more information, see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html) \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01e9af97-e4b3-40bc-a355-4cdfca965f07"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "891bcb1c-b6a2-4b44-af99-ff1deb5ab2e6",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.exportAuditRecords_get",
          "request": {
            "url": "{{default}}/audit/export?endDate=%7B%7D&format=%7B%7D&searchString=%7B%7D&startDate=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Exports audit records as a CSV file or ZIP file.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cefb1ed-e4d9-4629-9fa6-54af9740ad1f"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "9c16cb39-9da5-4e71-89ca-850c74e7e33e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getRetentionPeriod_get",
          "request": {
            "url": "{{default}}/audit/retention",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the retention period for records in the audit log. The retention \nperiod is how long an audit record is kept for, from creation date until \nit is deleted.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee6c3187-c4e2-40e6-be63-e339c46f1eed"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "f0417b6d-0e6a-4d77-98c5-69a66882c363",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.setRetentionPeriod_put",
          "request": {
            "url": "{{default}}/audit/retention",
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Sets the retention period for records in the audit log. The retention period \ncan be set to a maximum of 20 years.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "36530c1a-007c-487c-871f-c07d6d469506"
            }
          ]
        },
        {
          "id": "34a6a0ea-fda6-470f-9b4a-02e9f7d16692",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.setLookAndFeelSettings_put",
          "request": {
            "url": "{{default}}/settings/lookandfeel/selected?spaceKey=%7B%7D",
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Sets the look and feel settings to either the default settings or the\ncustom settings, for the site or a single space. Note, the default \nspace settings are inherited from the current global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5125d65-f36c-4358-85a7-eeeb59e0cb83"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "79a7d41f-1407-4c1e-a1e3-fa98d0007db7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContent_get",
          "request": {
            "url": "{{default}}/content?expand=%7B%7D&limit=%7B%7D&orderby=%7B%7D&postingDay=%7B%7D&spaceKey=%7B%7D&start=%7B%7D&status=%7B%7D&title=%7B%7D&trigger=%7B%7D&type=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all content in a Confluence instance.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission). \nOnly content that the user has permission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "133f46a1-1cd4-4a55-9fea-8cd1257d0e9b"
            }
          ]
        },
        {
          "id": "ee4a5dde-6911-49b4-8f30-b8fba684cb8e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.createContent_post",
          "request": {
            "url": "{{default}}/content?expand=%7B%7D&status=%7B%7D",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new piece of content or publishes an existing draft. \n\nTo publish a draft, add the `id` and `status` properties to the body of the request. \nSet the `id` to the ID of the draft and set the `status` to 'current'. When the \nrequest is sent, a new piece of content will be created and the metadata from the \ndraft will be transferred into it.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'Add' permission for the \nspace that the content will be created in, and permission to view the draft if publishing a draft."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "377d14bb-14ed-4151-b202-260b1cb7a54e"
            }
          ]
        },
        {
          "id": "6579ca7c-ab45-4734-991e-2536afb2012e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContentById_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "embeddedContentRender",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "trigger",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "version",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a single piece of content, like a page or a blog post.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3c69bf80-5a7f-4be3-afc0-40d14549a0e5"
            }
          ]
        },
        {
          "id": "eb783d38-95c5-4fc5-af41-9a1cbe7ded2a",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.updateContent_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "conflictPolicy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Updates a piece of content. Use this method to update the title or body \nof a piece of content, change the status, change the parent page, and more.\n\nNote, updating draft content is currently not supported.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a1487e11-84a2-4488-9937-c2720a92b54d"
            }
          ]
        },
        {
          "id": "732e3f60-4a97-437c-89cb-20083ae53d90",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.deleteContent_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Moves a piece of content to the space's trash or purges it from the trash, \ndepending on the content's type and status:\n\n- If the content's type is `page` or `blogpost` and its status is `current`, \nit will be trashed.\n- If the content's type is `page` or `blogpost` and its status is `trashed`, \nthe content will be purged from the trash and deleted permanently. Note, \nyou must also set the `status` query parameter to `trashed` in your request.\n- If the content's type is `comment` or `attachment`, it will be deleted \npermanently without being trashed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Delete' permission for the space that the content is in, and permission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28de10df-d110-423d-a30f-dc88fda309f7"
            }
          ]
        },
        {
          "id": "9390c2c1-0a9e-4fe5-acba-31f2d87bb464",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildren_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a map of the direct children of a piece of content. A piece of content \nhas different types of child content, depending on its type. These are \nthe default parent-child content type relationships:\n\n- `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n- `comment`: child content is `attachment`\n\nApps can override these default relationships. Apps can also introduce \nnew content types that create new parent-child content relationships.\n\nNote, the map will always include all child content types that are valid \nfor the content. However, if the content has no instances of a child content \ntype, the map will contain an empty array for that child content type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2377cecf-f028-4a7a-a573-c67ac0ae21a2"
            }
          ]
        },
        {
          "id": "3bfc547b-6129-42a0-adb3-7360338e9312",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentComments_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/comment"
              ],
              "query": [
                {
                  "key": "depth",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "location",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "858eca65-0636-4103-9a76-e3399b2faf68"
            }
          ]
        },
        {
          "id": "59bcc296-d988-4bd9-9010-c10841ba3c73",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildrenByType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/:type"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all children of a given type, for a piece of content. \nA piece of content has different types of child content, depending on its type:\n\n- `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n- `comment`: child content is `attachment`\n\nCustom content types that are provided by apps can also be returned.\n\nNote, this method only returns direct children. To return children at all \nlevels, use [Get descendants by type](#api-content-id-descendant-type-get).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "85ff14c4-5104-4f32-9aaa-4df8dc6fc963"
            }
          ]
        },
        {
          "id": "0515b5c1-1fd3-40f0-8f3d-dc45216536d5",
          "name": "com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.getContentDescendants_g",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/descendant"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a map of the descendants of a piece of content. This is similar \nto [Get content children](#api-content-id-child-get), except that this \nmethod returns child pages at all levels, rather than just the direct \nchild pages.\n\nA piece of content has different types of descendants, depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n- `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant is `comment`\n- `comment`: descendant is `attachment`\n\nThe map will always include all descendant types that are valid for the content. \nHowever, if the content has no instances of a descendant type, the map will \ncontain an empty array for that descendant type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it \nis a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "365efacb-73ea-40a8-b6d6-68b0f1f339ba"
            }
          ]
        },
        {
          "id": "e50773be-b926-4e9a-a01f-acba4202e85b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.descendantsOfType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/descendant/:type"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all descendants of a given type, for a piece of content. This is \nsimilar to [Get content children by type](#api-content-id-child-type-get), \nexcept that this method returns child pages at all levels, rather than just \nthe direct child pages.\n\nA piece of content has different types of descendants, depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n- `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant is `comment`\n- `comment`: descendant is `attachment`\n\nCustom content types that are provided by apps can also be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it \nis a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "440e8ed0-9641-4738-ab1b-73751c7252cf"
            }
          ]
        },
        {
          "id": "b662a8d8-001d-49e2-abd2-272797cb70fc",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperties_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the properties for a piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be0e72ce-35e9-43e0-9a82-ee7def96cf56"
            }
          ]
        },
        {
          "id": "986cf7ee-e3a5-4a5d-99aa-8bfe910b5ab4",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentProperty_pos",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a property for an existing piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis is the same as [Create content property for key](#api-content-id-property-key-post) \nexcept that the key is specified in the request body instead of as a \npath parameter.\n\nContent properties can also be added when creating a new piece of content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59be025d-cb5b-4e7c-9805-c15cc2f5fd92"
            }
          ]
        },
        {
          "id": "e2ed5cbd-4c87-4992-b572-b5d6bb62e3b6",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a content property for a piece of content. For more information, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "284a3684-d22a-4612-a298-8a74643fd4fa"
            }
          ]
        },
        {
          "id": "3c2783bf-f6d3-48ef-b114-bbf73d6e76f1",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.updateContentProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Updates an existing content property. This method will also create a new \nproperty for a piece of content, if the property key does not exist and \nthe property version is 1. For more information about content properties, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70885f68-5dfb-4116-9184-4ef21de9be2e"
            }
          ]
        },
        {
          "id": "bc37b4eb-bc61-47ed-8e72-bffcad712025",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentPropertyForK",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a property for an existing piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis is the same as [Create content property](#api-content-id-property-post) \nexcept that the key is specified as a path parameter instead of in the \nrequest body.\n\nContent properties can also be added when creating a new piece of content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "54266e15-d9d6-4e5f-bc86-181c10930efe"
            }
          ]
        },
        {
          "id": "6bf44430-426e-49e8-b25d-07fb46410f2f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.deleteContentProperty_del",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a content property. For more information about content properties, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8557f932-d494-4570-9e60-da11c9573e03"
            }
          ]
        },
        {
          "id": "c7d37549-919a-4041-ae42-26643fefff17",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/group/:groupName"
              ],
              "variable": [
                {
                  "id": "groupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns whether the specified content restriction applies to a group. \nFor example, if the 'admins' group has permission to read a page with an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0d59fb91-fb1e-4770-8d54-d6d690ec2c4c"
            }
          ]
        },
        {
          "id": "ccbe4446-905d-4969-ba05-6628cf7a57bf",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/user"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns whether the specified content restriction applies to a user. \nFor example, if the user 'admin' has permission to read a page with an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/user?username=admin`\n\nOne of `key`, `username`, or `accountId` must be specified as a query \nparameter to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e89b01b-7e2d-4813-af15-0d5ed45b59e3"
            }
          ]
        },
        {
          "id": "cb02dee7-8001-4e90-b1f4-7ab40d03d0bb",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the versions for a piece of content in descending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "482e3fd6-94e7-405e-92c6-abf352709884"
            }
          ]
        },
        {
          "id": "9bfe344e-057c-404b-87c2-2a63a6182db2",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersion_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version/:versionNumber"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a version for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2c039764-227d-4cdb-ad1e-12f558250573"
            }
          ]
        },
        {
          "id": "c90c5f13-f5ee-4079-aa28-725727fe138f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.deleteContentVersion_delet",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version/:versionNumber"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Delete a historical version. This does not delete the changes made to the \ncontent in that version, rather the changes for the deleted version are \nrolled up into the next version. Note, you cannot delete the current version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c07d357-e2bd-4ba8-92c0-e8ade5395554"
            }
          ]
        },
        {
          "id": "c079fe7c-eede-4be2-bbaf-b81f37163314",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getContentByTypeForSpace_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/content/:type"
              ],
              "query": [
                {
                  "key": "depth",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "spaceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all content of a given type, in a space. The returned content is\nordered by content ID in ascending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'View' permission for the space. Note, the returned list will only\ncontain content that the current user has permission to view."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba3be690-bebd-4686-a2ff-068a95bbc7c7"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "464518eb-8c9b-4458-a5f9-5e663259804f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishSharedDraft_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/blueprint/instance/:draftId"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "draftId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Publishes a shared draft of a page created from a blueprint.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the draft and 'Add' permission for the space that \nthe content will be created in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eecd6e29-58d7-46a3-8cd9-0e02b9e64eb2"
            }
          ]
        },
        {
          "id": "46b611e5-61f2-4812-bfe7-ed5de3c1473c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishLegacyDraft_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/blueprint/instance/:draftId"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "draftId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Publishes a legacy draft of a page created from a blueprint. Legacy drafts \nwill eventually be removed in favour of shared drafts. For now, this method \nworks the same as [Publish shared draft](#api-content-blueprint-instance-draftId-put).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the draft and 'Add' permission for the space that \nthe content will be created in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52790438-fb53-4392-a5c0-d1321110fe04"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "5f14c733-5ff7-485b-b585-e7eea339bedd",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.searchContentByCQL_get",
          "request": {
            "url": "{{default}}/content/search?cql=%7B%7D&cqlcontext=%7B%7D&expand=%7B%7D&limit=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the list of content that matches a Confluence Query Language \n(CQL) query. For information on CQL, see: \n[Advanced searching using CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission). \nOnly content that the user has permission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68c27397-0d83-4c5c-8e41-92db27e1c052"
            }
          ]
        },
        {
          "id": "2246f0a1-a6b0-4b55-8110-e58b02f65d4e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SearchResource.search_get",
          "request": {
            "url": "{{default}}/search?cql=%7B%7D&cqlcontext=%7B%7D&includeArchivedSpaces=%7B%7D&limit=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Searches for content using the \n[Confluence Query Language (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the entities. Note, only entities that the user has \npermission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7fa74f53-904c-472b-b854-3bed8161fa37"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachments",
      "item": [
        {
          "id": "60b229d2-4e31-46fe-a7b4-cff1bc02b904",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.getAttachments_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filename",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "mediaType",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the attachments for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d798c0a0-4e18-4923-a50a-ca15c4be26ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "94b67306-2118-4779-8002-6d0bae99d510",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createOrUpdateAttachments_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds an attachment to a piece of content. If the attachment already exists \nfor the content, then the attachment is updated (i.e. a new version of the \nattachment is created).\n\nNote, you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries have classes that make it easier to implement \nmultipart posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) \nJava class provided by Apache HTTP Components.\n\nExample: This curl command attaches a file ('example.txt') to a piece of \ncontent (id='123') with a comment and `minorEdits`=true. If the 'example.txt' \nfile already exists, it will update it with a new version of the attachment.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X PUT \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dffcbe39-dd79-4959-aca4-de4204abeb82"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "623f49d7-156c-48a4-9a39-4010e021d993",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createAttachments_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds an attachment to a piece of content. This method only adds a new \nattachment. If you want to update an existing attachment, use \n[Create or update attachments](#api-content-id-child-attachment-put).\n\nNote, you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries have classes that make it easier to implement \nmultipart posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) \nJava class provided by Apache HTTP Components.\n\nExample: This curl command attaches a file ('example.txt') to a container \n(id='123') with a comment and `minorEdits`=true.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
 
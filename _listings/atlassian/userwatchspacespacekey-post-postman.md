{
  "info": {
    "name": "Confluence Cloud API Add space watcher",
    "_postman_id": "0acadfea-2e3a-4813-bed3-40fae678f290",
    "description": "Adds a user as a watcher to a space. Choose the user by doing one of the \nfollowing:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "4994b559-4e72-426a-8bfc-86d7c174479f",
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
              "id": "7369488a-f5ed-4994-a410-47a67317bab1"
            }
          ]
        },
        {
          "id": "6fe0b00e-2d31-4308-87e6-6f18ea203fe7",
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
              "id": "90d1b88c-9b46-48c4-aec5-c2fbadaf188c"
            }
          ]
        },
        {
          "id": "ca73ee41-c76a-4304-85df-c61dd9bae715",
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
              "id": "99538c48-2a2f-40b8-be8e-eb143d84c30c"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "9111783f-3ef1-4537-9b9a-a5046778a6c1",
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
              "id": "a447abaa-98ff-42b8-a2a7-983d00c0b96e"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "48e4603b-45c0-4700-8e11-1f64c8e51fab",
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
              "id": "48ebebff-c32e-42f1-acd9-41dc7c98df2c"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "cb15c968-4aed-4a1e-ab17-d8b0be9529cc",
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
              "id": "67d055ad-3cf9-4141-8d31-3e38055049f8"
            }
          ]
        },
        {
          "id": "b6060f5e-0ccb-47a0-8bbc-9ace87d673e1",
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
              "id": "40b387ee-0c55-4137-8101-4918a702df4b"
            }
          ]
        },
        {
          "id": "bf6cfcca-b756-4b4f-abf2-69457163c608",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.setSpaceTheme_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/theme"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Sets the theme for a space. Note, if you want to reset the space theme to \nthe default Confluence theme, use the 'Reset space theme' method instead \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "456845c1-3070-4e13-bd0a-c68a594ac064"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "818b99cd-cc38-4861-92fd-40e7320299c9",
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
              "id": "47d2e73b-4a9e-4a4f-9ae6-7c13d1212b13"
            }
          ]
        },
        {
          "id": "dc1455a1-ca1e-4fcc-89db-96326c214f5c",
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
              "id": "729836ff-398d-4d05-9594-614f96ecb616"
            }
          ]
        },
        {
          "id": "d2456b64-fe1a-4c62-b4d2-3d1fc6254299",
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
              "id": "dc233536-a737-4773-8fd4-66ad37f184d6"
            }
          ]
        },
        {
          "id": "9348d8d5-74f3-4b82-8550-c6247d3a0294",
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
              "id": "91b8e052-10c2-425c-b950-c55685322702"
            }
          ]
        },
        {
          "id": "99a004d8-96eb-47ae-b0a5-05c9e5683423",
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
              "id": "d6ec1f2c-faf3-44f9-aa1c-db22804bf849"
            }
          ]
        },
        {
          "id": "369e3b71-cb30-4b66-a18a-95db3440324b",
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
              "id": "05475f6a-9c97-4a20-9766-0e6d700bba42"
            }
          ]
        },
        {
          "id": "de1a484d-1944-46b8-8fc5-1f70961f7f2d",
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
              "id": "5e0e58e1-37d3-42a3-9267-142d7d85541a"
            }
          ]
        },
        {
          "id": "5d3596d2-14f9-4715-a2fa-92a73f051a41",
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
              "id": "f72c706c-f02f-4b92-a92c-d6c72790ef77"
            }
          ]
        },
        {
          "id": "157dc6b0-9d79-4047-bf5b-9d69788887e9",
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
              "id": "6c068aab-7235-4651-9087-6df4052337b2"
            }
          ]
        },
        {
          "id": "539be1bc-113e-4588-ad90-28c98455e05f",
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
              "id": "8cf35713-a113-496b-9337-5b3b614a1468"
            }
          ]
        },
        {
          "id": "c347dd63-f454-49b9-814f-ac68ebb947e1",
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
              "id": "8884257f-d96e-4fb7-b0b3-0a94cd3d50c5"
            }
          ]
        },
        {
          "id": "2dad300d-0d61-41b5-a668-db99a7b9ec05",
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
              "id": "4fa379a8-9880-4fea-8574-e39d8ce13113"
            }
          ]
        },
        {
          "id": "49c4e76b-c3cd-4b50-8edc-f62e3b7e9efd",
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
              "id": "f42a841c-827c-4e48-85ca-9b04ec084903"
            }
          ]
        },
        {
          "id": "b7be49c9-093d-4dde-8216-3b5e4f3c4e19",
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
              "id": "08f18298-df1e-4f0e-98d0-0a0d79f566dc"
            }
          ]
        },
        {
          "id": "fbb22391-9a74-4b37-82fb-9979e456abd8",
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
              "id": "f7cd3a25-3b2b-49e6-be52-81978d95abbc"
            }
          ]
        },
        {
          "id": "974558ff-33c5-42a5-ae73-4042f4a95500",
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
              "id": "4f680d32-3423-4118-857d-1b0e0a8e31f2"
            }
          ]
        },
        {
          "id": "a7371408-0a7f-4b19-b8c1-93719af6e137",
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
              "id": "30c54a11-577b-48c5-9380-0b1e33cf80da"
            }
          ]
        },
        {
          "id": "509e47df-deae-4ae9-b4e4-b06ecee87d3d",
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
              "id": "bd2049c0-acf0-4c34-a0be-efbaab02475e"
            }
          ]
        },
        {
          "id": "cb684e3e-2ac7-4696-8827-92048be8f556",
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
              "id": "d74dd1fa-7669-4208-a43e-02f05862e529"
            }
          ]
        },
        {
          "id": "b07af7fd-5245-4ec8-bf83-4dae43c39d29",
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
              "id": "59921dc5-b3bc-4626-9c08-ed18c8749249"
            }
          ]
        },
        {
          "id": "65779279-0a9d-4659-969b-8d460651e285",
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
              "id": "99662b3e-6ba7-48e2-9165-3841c5996d1a"
            }
          ]
        },
        {
          "id": "ba05118c-2c7c-4e6c-a487-985c50fbf37e",
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
              "id": "5c42fbec-a248-4ef3-9218-83b010302f04"
            }
          ]
        },
        {
          "id": "70a2d087-af15-4774-8c55-11f7092bd449",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.updateContentTemplate_put",
          "request": {
            "url": "{{default}}/template",
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
            "description": "Updates a content template. Note, blueprint templates cannot be updated\nvia the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to create a space template or 'Confluence Administrator' \nglobal permission to create a global template."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bdcda02b-11d9-4661-8f2c-d96706ae0eaf"
            }
          ]
        },
        {
          "id": "5081cda2-2aef-40b8-aeea-46bac8f7e6cb",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.createContentTemplate_post",
          "request": {
            "url": "{{default}}/template",
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
            "description": "Creates a new content template. Note, blueprint templates cannot be created via the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to create a space template or 'Confluence Administrator' \nglobal permission to create a global template."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c2474d5-5dab-47f9-93fd-d7cfe9e596e1"
            }
          ]
        },
        {
          "id": "ebc17cb7-a2be-4955-aef7-38258af74af8",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplates_get",
          "request": {
            "url": "{{default}}/template/page?expand=%7B%7D&limit=%7B%7D&spaceKey=%7B%7D&start=%7B%7D",
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
            "description": "Returns all content templates. Use this method to retrieve all global\ncontent templates or all content templates in a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to view space templates and 'Confluence \nAdministrator' global permission to view global templates."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2b33ad38-f7cb-4594-b0ab-477831991ce9"
            }
          ]
        },
        {
          "id": "e6955c9f-7ffd-45b9-9d1d-95bfa5d938ed",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplate_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "template/:contentTemplateId"
              ],
              "variable": [
                {
                  "id": "contentTemplateId",
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
            "description": "Returns a content template. This includes information about template, \nlike the name, the space or blueprint that the template is in, the body \nof the template, and more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to view space templates and 'Confluence \nAdministrator' global permission to view global templates."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51bebdd4-90e4-4933-8bc4-c2d730427538"
            }
          ]
        },
        {
          "id": "91ed0bb6-c50e-45ab-a29c-0258f00793d6",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.getContentWatchStatus_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/watch/content/:contentId"
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
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contentId",
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
            "description": "Returns whether a user is watching a piece of content. Choose the user by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06972cea-482b-4028-bd55-abe18a820570"
            }
          ]
        },
        {
          "id": "11efe801-1662-4e27-b42f-4aefde2b0b19",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addContentWatcher_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/watch/content/:contentId"
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
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contentId",
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
            "description": "Adds a user as a watcher to a piece of content. Choose the user by doing \none of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ce97b28f-4cfd-4e42-922d-7c6c90f7b331"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "21945d67-c287-4ecd-8f5f-7fbb1ecd10dc",
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
              "id": "18f326b2-736e-4e9d-80d2-6b251e59675e"
            }
          ]
        },
        {
          "id": "af90e02f-8b90-4ee2-abb6-7be165e9c1b1",
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
       
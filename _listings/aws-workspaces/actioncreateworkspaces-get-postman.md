{
  "info": {
    "name": "AWS WorkSpaces Service API Create Workspaces",
    "_postman_id": "30c71faf-70f1-47b1-9a04-ca9c5457eb54",
    "description": "Creates one or more WorkSpaces.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Tags",
      "item": [
        {
          "id": "deb18576-35dc-4ea6-8e8a-04f292a142cb",
          "name": "createTags",
          "request": {
            "url": "http://example.com/api/?Action=CreateTags?ResourceId=ResourceId&Tags=Tags",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates tags for a WorkSpace."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2445bb87-0cfa-4156-aef0-b48f0f6ac727"
            }
          ]
        }
      ]
    },
    {
      "name": "Folder",
      "item": [
        {
          "id": "9c885379-7f75-4204-b1d8-fb529f46f791",
          "name": "createWorkspaces",
          "request": {
            "url": "http://example.com/api/?Action=CreateWorkspaces?Workspaces=Workspaces",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates one or more WorkSpaces."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f294b6d4-1ea0-4ec6-9b64-b90d15cc1c60"
            }
          ]
        }
      ]
    }
  ]
}
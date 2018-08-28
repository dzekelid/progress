{
  "info": {
    "name": "Quovo Get a connection's sync progress",
    "_postman_id": "3d9ef750-a0d7-4b30-a055-212bd61c92f4",
    "description": "Check the ongoing Sync progress of an Account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Connections",
      "item": [
        {
          "id": "465d7733-15c8-40e9-936f-30a8c1a9227f",
          "name": "ConnectionsSyncByConnectionIdGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "connections/:connection_id/sync"
              ],
              "variable": [
                {
                  "id": "connection_id",
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
            "description": "Check the ongoing Sync progress of an Account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2fa1f1f3-eeab-4846-a88f-7002cee67c46"
            }
          ]
        }
      ]
    }
  ]
}
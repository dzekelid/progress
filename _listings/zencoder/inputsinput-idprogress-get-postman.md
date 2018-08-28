{
  "info": {
    "name": "Zencoder API Input Progress",
    "_postman_id": "1c88cd72-df13-49ae-a53e-348b93a95797",
    "description": "The return will contain one or more of the following keys: state, current_event, current_event_progress and progress.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Account",
      "item": [
        {
          "id": "eb4cb1d0-5dab-40b7-8326-3b80a9ebbff4",
          "name": "getAccount",
          "request": {
            "url": "http://app.zencoder.com/api/v2/account?api_key=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Account Details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7554ed81-c503-488b-a36d-53dbb732ea51"
            }
          ]
        },
        {
          "id": "9293ef3e-8e15-41f1-896d-856bafc6a1fa",
          "name": "postAccount",
          "request": {
            "url": "http://app.zencoder.com/api/v2/account?email=%7B%7D&password=%7B%7D&password_confirmation=%7B%7D&terms_of_service=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create an Account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5dfd3b2c-6f57-45a4-a232-48eaf90cebbe"
            }
          ]
        },
        {
          "id": "5266411b-8e5c-4dc9-bc56-86264f32293c",
          "name": "putAccountIntegration",
          "request": {
            "url": "http://app.zencoder.com/api/v2/account/integration?api_key=%7B%7D",
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Integration Mode"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58925a2d-cd39-4b77-9ac6-ccd466f09ec4"
            }
          ]
        },
        {
          "id": "4ff4e7c8-83ac-4913-a2ee-df33fb31893d",
          "name": "putAccountLive",
          "request": {
            "url": "http://app.zencoder.com/api/v2/account/live",
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Integration Mode - Live"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89e833ba-fc2e-422f-b59b-2f6d0a847611"
            }
          ]
        }
      ]
    },
    {
      "name": "Inputs",
      "item": [
        {
          "id": "49fc5b8b-8cf2-4e94-a283-75319ce3da1b",
          "name": "getInupdatesInupdate",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "inputs/:input_id"
              ],
              "query": [
                {
                  "key": "api_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "input_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Input Details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad403bca-8c07-4295-9f27-5b14a88169d5"
            }
          ]
        },
        {
          "id": "adedf3ea-fd4d-4cb3-af42-1f144eef6f31",
          "name": "getInupdatesInupdateProgress",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "inputs/:input_id/progress"
              ],
              "variable": [
                {
                  "id": "input_id",
                  "value": "input_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The return will contain one or more of the following keys: state, current_event, current_event_progress and progress."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c45cec5f-ef3f-40cc-af1e-01d1ea328821"
            }
          ]
        }
      ]
    }
  ]
}
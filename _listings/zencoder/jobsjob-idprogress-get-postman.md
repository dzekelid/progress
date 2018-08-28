{
  "info": {
    "name": "Zencoder API Job Progress",
    "_postman_id": "17fe7b43-18d3-48b3-93ea-727a08ba58ec",
    "description": "The return will contain one or more of the following keys: state, input, outputs, and progress.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Account",
      "item": [
        {
          "id": "4e8b6f9e-7eb2-4edd-9226-3f42d185e288",
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
              "id": "331377f1-b352-4a22-8859-ae168a916a8b"
            }
          ]
        },
        {
          "id": "c2b20039-7287-49c5-a550-d692e056201c",
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
              "id": "ad4cc9e5-484c-4699-81d7-4da04a37296c"
            }
          ]
        },
        {
          "id": "ccd1c614-a9d8-4489-9090-d184662eab74",
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
              "id": "458682d6-2157-4956-a0d9-0530cd234a2e"
            }
          ]
        },
        {
          "id": "ed607d8b-a5c5-47d7-9ee5-213819888ff9",
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
              "id": "083be220-129f-4801-adfa-f5b12983078f"
            }
          ]
        }
      ]
    },
    {
      "name": "Inputs",
      "item": [
        {
          "id": "5b0b0ca5-40e0-49d8-ab1b-413be1fb8943",
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
              "id": "897a7f43-e60f-4bbd-8112-46de3148bcb5"
            }
          ]
        },
        {
          "id": "a3c0ed3b-32ab-49a8-a370-241361036e47",
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
              "id": "3cf07b2c-34a7-4337-9033-37992c6ae093"
            }
          ]
        }
      ]
    },
    {
      "name": "Jobs",
      "item": [
        {
          "id": "90d88e07-d0c1-464b-9cf9-b5f2b5bc170b",
          "name": "getJobs",
          "request": {
            "url": "http://app.zencoder.com/api/v2/jobs?api_key=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A list of jobs can be obtained by sending an HTTP GET request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6bde9a00-20c5-40bf-b980-707594220b5c"
            }
          ]
        },
        {
          "id": "00b55ea0-a710-49bf-8c62-5e5e0bb38502",
          "name": "postJobs",
          "request": {
            "url": "http://app.zencoder.com/api/v2/jobs?api_key=%7B%7D&Encoding Settings=%7B%7D&input=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Encoding jobs are created by sending an HTTP POST request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d29a3dad-fb98-4684-99e8-de527b9301b3"
            }
          ]
        },
        {
          "id": "2f51e033-eae8-491f-8942-6493af8d5ff2",
          "name": "getJobsJob",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "jobs/:job_id"
              ],
              "query": [
                {
                  "key": "api_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "Get Job Details",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "job_id",
                  "value": "job_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Job Details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a463a2bf-763c-4d95-8f6e-6190cbf9b30e"
            }
          ]
        },
        {
          "id": "aea78e28-dea8-4ef0-9ff2-c4a259c83f1e",
          "name": "putJobsJobCancel",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "jobs/:job_id/cancel"
              ],
              "query": [
                {
                  "key": "api_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "job_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "If you wish to cancel a job that has not yet finished processing you may send a request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f251975-9a10-4884-8de8-447f5e330e01"
            }
          ]
        },
        {
          "id": "e160d6b8-d7db-420f-88eb-05938d47fbfb",
          "name": "putJobsJobFinish",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "jobs/:job_id/finish"
              ],
              "variable": [
                {
                  "id": "job_id",
                  "value": "job_id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Finishes the input on a Live streaming job."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "21cc9728-a915-459d-8980-07346b783e27"
            }
          ]
        },
        {
          "id": "7a7a3901-714f-4f57-90f0-59e333118fa4",
          "name": "getJobsJobProgress",
          "request": {
            "url": {
              "protocol": "http",
              "host": "app.zencoder.com",
              "path": [
                "api",
                "v2",
                "jobs/:job_id/progress"
              ],
              "variable": [
                {
                  "id": "job_id",
                  "value": "job_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The return will contain one or more of the following keys: state, input, outputs, and progress."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fdd32e55-a3d0-4258-bbaf-d75e00fc4f49"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "Instructure Canvas Utility APIs Query progress",
    "_postman_id": "0dfee56c-eda6-4e32-97ab-703a1e4f4f8c",
    "description": "Query progress.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Api",
      "item": [
        {
          "id": "cf697dbc-5782-46e3-9d79-f8046344de3d",
          "name": "retrieve-assignments-enabled-for-grade-export-to-sis",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "api/sis/accounts/:account_id/assignments"
              ],
              "query": [
                {
                  "key": "course_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ends_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "starts_before",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "account_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve assignments enabled for grade export to sis."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b6756cc8-56f2-4d9e-a7a9-56b736cc2972"
            }
          ]
        },
        {
          "id": "cd20fe57-9014-4224-9003-40045224db85",
          "name": "retrieve-assignments-enabled-for-grade-export-to-sis1",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "api/sis/courses/:course_id/assignments"
              ],
              "query": [
                {
                  "key": "account_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ends_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "starts_before",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "course_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve assignments enabled for grade export to sis."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d357f9cc-6ac5-4bc5-8b98-0ea0e235e522"
            }
          ]
        }
      ]
    },
    {
      "name": "Collaborations",
      "item": [
        {
          "id": "71331a22-bd78-434f-bc96-d652b56c3fc1",
          "name": "list-members-of-a-collaboration",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "collaborations/:id/members"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List members of a collaboration.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6682a677-0c66-4efd-a3b8-50bceb8be73a"
            }
          ]
        }
      ]
    },
    {
      "name": "Comm",
      "item": [
        {
          "id": "4b427369-d1d6-43dc-a02f-59e1f3a99db8",
          "name": "list-of-commmessages-for-a-user",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/comm_messages?end_time=%7B%7D&start_time=%7B%7D&user_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List of commmessages for a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd6d1da0-ebec-46f4-b199-522f6eb09be6"
            }
          ]
        }
      ]
    },
    {
      "name": "Course",
      "item": [
        {
          "id": "2deb19fc-bcc9-4643-a195-7a4e55921953",
          "name": "list-accounts-for-course-admins",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/course_accounts",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List accounts for course admins."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e56c2239-a655-4178-9f02-f5fd3b899c5a"
            }
          ]
        }
      ]
    },
    {
      "name": "Error",
      "item": [
        {
          "id": "275923ac-0354-41c7-8cc9-a7e4fb6f9db1",
          "name": "create-error-report",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/error_reports?error[comments]=%7B%7D&error[email]=%7B%7D&error[http_env]=%7B%7D&error[subject]=%7B%7D&error[url]=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create error report."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1bd2ffb7-3f92-4be5-9702-f7273cdc8f8c"
            }
          ]
        }
      ]
    },
    {
      "name": "Jwts",
      "item": [
        {
          "id": "fb9bc8b4-b8e7-4d5f-87c9-f635461313cf",
          "name": "create-jwt",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/jwts",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create jwt."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9dd9b24e-9d10-47bf-aa31-6d4b075d917f"
            }
          ]
        }
      ]
    },
    {
      "name": "Outcomes",
      "item": [
        {
          "id": "43f72bb7-4855-4b73-ae18-378c235f9131",
          "name": "show-an-outcome",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "outcomes/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Show an outcome."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "29f537dc-805e-4da1-a938-d2786a5889f1"
            }
          ]
        },
        {
          "id": "64a98356-c64a-402f-9004-b049f7424ca0",
          "name": "update-an-outcome",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "outcomes/:id"
              ],
              "query": [
                {
                  "key": "calculation_int",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "calculation_method",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "description",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "display_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "mastery_points",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ratings[][description]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ratings[][points]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "title",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "vendor_guid",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Update an outcome."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26c912ac-ed98-4822-a1ee-f6005831fc41"
            }
          ]
        }
      ]
    },
    {
      "name": "Progress",
      "item": [
        {
          "id": "c7615616-1609-4c7f-a489-0c6edfdb2226",
          "name": "query-progress",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "progress/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Query progress."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eede543a-f5f3-4cdd-84ac-fbcf4abb9af9"
            }
          ]
        }
      ]
    }
  ]
}
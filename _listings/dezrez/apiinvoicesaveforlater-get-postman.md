{
  "info": {
    "name": "Dezrez Return list of receipts progress amounts",
    "_postman_id": "c5c16bbc-06c3-4479-b4f7-0d5bac383499",
    "description": "Return list of receipts progress amounts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Return",
      "item": [
        {
          "id": "592aed0c-1002-4ad3-b181-11f494e8997f",
          "name": "Invoice_SaveForLater",
          "request": {
            "url": "http://api.dezrez.com/api/invoice/saveforlater",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Return list of receipts progress amounts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac31cb73-b2c9-469f-933e-bcac824954e9"
            }
          ]
        }
      ]
    }
  ]
}
---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Save expected receipts progress
  version: 1.0.0
  description: Save expected receipts progress.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/invoice/saveforlater:
    get:
      summary: Return list of receipts progress amounts
      description: Return list of receipts progress amounts.
      operationId: Invoice_SaveForLater
      x-api-path-slug: apiinvoicesaveforlater-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Return
      - List
      - Of
      - Receipts
      - Progress
      - Amounts
    post:
      summary: Save expected receipts progress
      description: Save expected receipts progress.
      operationId: Invoice_SaveForLaterByreceipts
      x-api-path-slug: apiinvoicesaveforlater-post
      parameters:
      - in: body
        name: receipts
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - Expected
      - Receipts
      - Progress
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
---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay View In-Progress Batches
  description: View only recent in-progress import batches.
  contact:
    name: VersaPay Support
    url: https://www.versapay.com/support
    email: support@versapay.com
  version: 1.0.0
host: secure.versapay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/imports:
    get:
      summary: View In-Progress & Completed Batches
      description: View recent in-progress and completed import batches.
      operationId: viewAllBatches
      x-api-path-slug: apiimports-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - In-Progress
      - '&'
      - Completed
      - Batches
  /api/imports/processing:
    get:
      summary: View In-Progress Batches
      description: View only recent in-progress import batches.
      operationId: viewInProgressBatches
      x-api-path-slug: apiimportsprocessing-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - In-Progress
      - Batches
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
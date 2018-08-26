---
swagger: "2.0"
x-collection-name: Zencoder
x-complete: 0
info:
  title: Zencoder API Input Progress
  version: v2
  description: 'The return will contain one or more of the following keys: state,
    current_event, current_event_progress and progress.'
host: app.zencoder.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /inputs/{input_id}/progress:
    get:
      summary: Input Progress
      description: 'The return will contain one or more of the following keys: state,
        current_event, current_event_progress and progress.'
      operationId: getInupdatesInupdateProgress
      x-api-path-slug: inputsinput-idprogress-get
      responses:
        200:
          description: OK
      tags:
      - Inputs
      - Input
      - Id
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
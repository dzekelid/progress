---
swagger: "2.0"
x-collection-name: AWS Data Pipeline
x-complete: 0
info:
  title: AWS Data Pipeline API Report Task Progress
  version: 1.0.0
  description: Task runners call ReportTaskProgress when assigned a task to acknowledge
    that it has the task.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ReportTaskProgress:
    get:
      summary: Report Task Progress
      description: Task runners call ReportTaskProgress when assigned a task to acknowledge
        that it has the task.
      operationId: reportTaskProgress
      x-api-path-slug: actionreporttaskprogress-get
      parameters:
      - in: query
        name: fields
        description: Key-value pairs that define the properties of the ReportTaskProgressInput
          object
        type: string
      - in: query
        name: taskId
        description: The ID of the task assigned to the task runner
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tasks
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
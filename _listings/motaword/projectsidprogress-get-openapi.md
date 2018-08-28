---
swagger: "2.0"
x-collection-name: MotaWord
x-complete: 0
info:
  title: Mota Word Get project progress
  description: Get the progress of an already launched project.
  version: alpha-0.1.0
host: api.motaword.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /projects/{id}/progress:
    get:
      summary: Get project progress
      description: Get the progress of an already launched project.
      operationId: getProgress
      x-api-path-slug: projectsidprogress-get
      parameters:
      - in: path
        name: id
        description: Project ID
      responses:
        200:
          description: OK
      tags:
      - Projects
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
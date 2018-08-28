swagger: "2.0"
x-collection-name: Zencoder
x-complete: 1
info:
  title: Zencoder
  version: v2
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
  /jobs/{job_id}/progress:
    get:
      summary: Job Progress
      description: 'The return will contain one or more of the following keys: state,
        input, outputs, and progress.'
      operationId: getJobsJobProgress
      x-api-path-slug: jobsjob-idprogress-get
      responses:
        200:
          description: OK
      tags:
      - Jobs
      - Job
      - Id
      - Progress
  /outputs/{output_id}/progress:
    get:
      summary: Output Progress
      description: 'The return will contain one or more of the following keys: state,
        current_event, current_event_progress and progress.'
      operationId: getOutupdatesOutupdateProgress
      x-api-path-slug: outputsoutput-idprogress-get
      parameters:
      - in: query
        name: api_key
        description: The API key
      - in: query
        name: callback
        description: JSONP Callback
      - in: query
        name: output_id
        description: The output id
      responses:
        200:
          description: OK
      tags:
      - Outputs
      - Output
      - Id
      - Progress
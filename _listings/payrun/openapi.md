swagger: "2.0"
x-collection-name: PayRun
x-complete: 1
info:
  title: Pay Run.IO
  description: open-scableable-transparent-payroll-api-
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Jobs/Dps/{JobId}/Progress:
    get:
      summary: Get the DPS job progress
      description: Return the the DPS job progress
      operationId: GetDpsJobProgress
      x-api-path-slug: jobsdpsjobidprogress-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: JobId
        description: The job unique identifier
      responses:
        200:
          description: OK
      tags:
      - DPJob
      - Progress
  /Jobs/PayRuns/{JobId}/Progress:
    get:
      summary: Get the pay run job progress
      description: Return the the payrun job progress
      operationId: GetPayRunJobProgress
      x-api-path-slug: jobspayrunsjobidprogress-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: JobId
        description: The job unique identifier
      responses:
        200:
          description: OK
      tags:
      - Pay
      - Run
      - Job
      - Progress
  /Jobs/Rti/{JobId}/Progress:
    get:
      summary: Get the RTI job progress
      description: Return the the RTI job progress
      operationId: GetRtiJobProgress
      x-api-path-slug: jobsrtijobidprogress-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: JobId
        description: The job unique identifier
      responses:
        200:
          description: OK
      tags:
      - RTI
      - Job
      - Progress
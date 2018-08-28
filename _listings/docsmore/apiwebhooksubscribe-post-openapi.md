---
swagger: "2.0"
x-collection-name: Docsmore
x-complete: 0
info:
  title: Docsmore Subscribe To Webhook
  description: |-
    Make sure you have a unique payload URL every time you use this api call to register your webhook. Unable to do so will result in webhook registration denial.


    For multiple events subscription, just use it comma separated values. Here are the available list of register events.



    documentUploadComplete
    workflowProgressEvent
    workflowCompleteEvent
    documentflowProgressEvent
    documentflowCompleteEvent
    documentSelfSigninCompleteEvent
  version: "1.0"
host: api.docsmore.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/webhook/subscribe:
    post:
      summary: Subscribe To Webhook
      description: |-
        Make sure you have a unique payload URL every time you use this api call to register your webhook. Unable to do so will result in webhook registration denial.


        For multiple events subscription, just use it comma separated values. Here are the available list of register events.



        documentUploadComplete
        workflowProgressEvent
        workflowCompleteEvent
        documentflowProgressEvent
        documentflowCompleteEvent
        documentSelfSigninCompleteEvent
      operationId: ApiWebhookSubscribePost
      x-api-path-slug: apiwebhooksubscribe-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Subscribe
      - Webhook
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
swagger: "2.0"
x-collection-name: Docsmore
x-complete: 1
info:
  title: Docsmore API 2.1
  description: alt-texthttpswww-docsmore-comwpcontentuploads201802docsmoreapi-png-titleh3create-a-developer-account-at-docsmore-io-and-start-unleashing-the-power-of-docsmore-into-your-own-applications--to-make-it-easier-we-have-provided-client-libraries-and-sdk-in-several-languages-for-you-to-get-started-and-hit-the-ground-running-in-no-time-h3brbrh4note-if-you-dont-see-api-setting-under-top-right-menu-that-means-you-will-need-to-be-a-developer-account--please-contact-supportdocsmore-com-and-a-customer-service-expert-will-switch-your-account-to-developer-account--h4brbrh5just-head-over-to-httpsdocsmore-io-and-sign-up-for-your-30-days-trial-h5
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
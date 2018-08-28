swagger: "2.0"
x-collection-name: MotaWord
x-complete: 1
info:
  title: Mota Word
  description: use-motaword-api-to-post-and-track-your-translation-projects-
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
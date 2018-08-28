---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Delete milestone on Progression role
  version: 1.0.0
  description: Delete milestone on progression role.
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
  /api/reconcile/save:
    put:
      summary: Save current reconcile progress
      description: Save current reconcile progress.
      operationId: Reconcile_SaveByreconcileDataContract
      x-api-path-slug: apireconcilesave-put
      parameters:
      - in: body
        name: reconcileDataContract
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
      - Current
      - Reconcile
      - Progress
  /api/progression/savecontact:
    post:
      summary: Add a new contact to the given progression Role or edit an existing
        contact
      description: Add a new contact to the given progression role or edit an existing
        contact.
      operationId: Progression_SaveProgressionContactBysaveContactDataContract
      x-api-path-slug: apiprogressionsavecontact-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: saveContactDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Contact
      - To
      - Given
      - Progression
      - Role
      - Edit
      - Existing
      - Contact
  /api/progression/removecontact:
    post:
      summary: Remove an existing progression contact from the progression role
      description: Remove an existing progression contact from the progression role.
      operationId: Progression_RemoveProgressionContactByremoveContactDataContract
      x-api-path-slug: apiprogressionremovecontact-post
      parameters:
      - in: body
        name: removeContactDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Existing
      - Progression
      - Contact
      - From
      - Progression
      - Role
  /api/progression/getallcontacts:
    get:
      summary: Get all progression contacts for the given progression role
      description: Get all progression contacts for the given progression role.
      operationId: Progression_GetAllProgressionContactsByprogressionRoleIdBypageSizeBypageNumberByprogressionRoleType
      x-api-path-slug: apiprogressiongetallcontacts-get
      parameters:
      - in: query
        name: pageNumber
        description: The page of contacts to return
      - in: query
        name: pageSize
        description: The number of contacts to return
      - in: query
        name: progressionRoleId
        description: The Id of progression role to get all contacts for
      - in: query
        name: progressionRoleType
        description: The progression role type
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Contactsthe
      - Given
      - Progression
      - Role
  /api/progression/getallmilestones:
    get:
      summary: Get all progression milestones for the given progression role
      description: Get all progression milestones for the given progression role.
      operationId: Progression_GetAllProgressionMilestonesByprogressionRoleIdBypageSizeBypageNumberBymilestoneLeaseType
      x-api-path-slug: apiprogressiongetallmilestones-get
      parameters:
      - in: query
        name: milestoneCategoryType
      - in: query
        name: milestoneLeaseType
      - in: query
        name: milestoneStatus
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: query
        name: progressionRoleId
      - in: query
        name: progressionRoleType
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Milestonesthe
      - Given
      - Progression
      - Role
  /api/progression/milestonessummary:
    get:
      summary: Get a progression milestone summary for the given progression role
      description: Get a progression milestone summary for the given progression role.
      operationId: Progression_MilestonesSummaryByprogressionRoleIdBymilestoneLeaseTypeBymilestoneCategoryType
      x-api-path-slug: apiprogressionmilestonessummary-get
      parameters:
      - in: query
        name: milestoneCategoryType
      - in: query
        name: milestoneLeaseType
      - in: query
        name: progressionRoleId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Milestone
      - Summarythe
      - Given
      - Progression
      - Role
  /api/progression/{id}/deletemilestone/{milestoneId}:
    delete:
      summary: Delete milestone on Progression role
      description: Delete milestone on progression role.
      operationId: Progression_DeleteProgressionMilestoneByidBymilestoneId
      x-api-path-slug: apiprogressioniddeletemilestonemilestoneid-delete
      parameters:
      - in: path
        name: id
        description: Progression Role Id
      - in: path
        name: milestoneId
        description: Milestone Id to be deleted
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Milestone
      - "On"
      - Progression
      - Role
  /api/progression/milestone/addnote:
    post:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_AddMilestoneNoteBynoteDataContract
      x-api-path-slug: apiprogressionmilestoneaddnote-post
      parameters:
      - in: body
        name: noteDataContract
        description: Notes to be added
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/progression/milestones/reset:
    put:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_ResetRoleMilestonesBypurchasingRoleIdByroleId
      x-api-path-slug: apiprogressionmilestonesreset-put
      parameters:
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: roleId
        description: Sales role ID
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/progressionchain/{id}:
    get:
      summary: Get the progression chain for purchasing role
      description: Get the progression chain for purchasing role.
      operationId: ProgressionChain_GetByid
      x-api-path-slug: apiprogressionchainid-get
      parameters:
      - in: path
        name: id
        description: Purchasing Role Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Chainpurchasing
      - Role
  /api/progressionchain/{id}/createchain:
    post:
      summary: Create chain for sales progression role
      description: Create chain for sales progression role.
      operationId: ProgressionChain_CreateChainByid
      x-api-path-slug: apiprogressionchainidcreatechain-post
      parameters:
      - in: path
        name: id
        description: PurchasingRoleId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Chainsales
      - Progression
      - Role
  /api/progressionchain/{id}/addchainnode:
    post:
      summary: Add node to progression chain
      description: Add node to progression chain.
      operationId: ProgressionChain_AddChainNodesBydataContractByid
      x-api-path-slug: apiprogressionchainidaddchainnode-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Node
      - To
      - Progression
      - Chain
  /api/progressionchain/{id}/addchainlink:
    post:
      summary: Add node to progression chain
      description: Add node to progression chain.
      operationId: ProgressionChain_AddChainLinkBydataContractByid
      x-api-path-slug: apiprogressionchainidaddchainlink-post
      parameters:
      - in: body
        name: dataContract
        description: The chain link information
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Node
      - To
      - Progression
      - Chain
  /api/progressionchain/{id}/deletenode:
    put:
      summary: Add node to progression chain
      description: Add node to progression chain.
      operationId: ProgressionChain_DeleteNodeByidBydataContract
      x-api-path-slug: apiprogressionchainiddeletenode-put
      parameters:
      - in: body
        name: dataContract
        description: Delete node data contract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Node
      - To
      - Progression
      - Chain
  /api/progressionchain/{id}/deletechainlink:
    put:
      summary: Add node to progression chain
      description: Add node to progression chain.
      operationId: ProgressionChain_DeleteChainLinkByidBylinkId
      x-api-path-slug: apiprogressionchainiddeletechainlink-put
      parameters:
      - in: path
        name: id
      - in: query
        name: linkId
        description: The Id of the link to delete
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Node
      - To
      - Progression
      - Chain
  /api/progressionchain/{id}/resetchain:
    put:
      summary: Add node to progression chain
      description: Add node to progression chain.
      operationId: ProgressionChain_ResetChainByid
      x-api-path-slug: apiprogressionchainidresetchain-put
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Node
      - To
      - Progression
      - Chain
  /api/progressionchain/{id}/getchain:
    get:
      summary: Create chain for sales progression role
      description: Create chain for sales progression role.
      operationId: ProgressionChain_GetProgressionChainByid
      x-api-path-slug: apiprogressionchainidgetchain-get
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Chainsales
      - Progression
      - Role
  /api/progressionchain/{id}/create:
    post:
      summary: Create chain for sales progression role
      description: Create chain for sales progression role.
      operationId: ProgressionChain_CreateByid
      x-api-path-slug: apiprogressionchainidcreate-post
      parameters:
      - in: path
        name: id
        description: PurchasingRoleId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Chainsales
      - Progression
      - Role
  /api/progressionchain/{id}/additem:
    post:
      summary: Add item to sales progression chain
      description: Add item to sales progression chain.
      operationId: ProgressionChain_AddItemToChainByidBydataContract
      x-api-path-slug: apiprogressionchainidadditem-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Progression Role Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Item
      - To
      - Sales
      - Progression
      - Chain
  /api/progressionchain/{id}/updateitem:
    put:
      summary: Update item in sales progression chain
      description: Update item in sales progression chain.
      operationId: ProgressionChain_UpdateChainItemByidBydataContract
      x-api-path-slug: apiprogressionchainidupdateitem-put
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Progression Role Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Item
      - In
      - Sales
      - Progression
      - Chain
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
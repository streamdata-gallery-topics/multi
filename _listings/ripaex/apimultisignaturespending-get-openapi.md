---
swagger: "2.0"
x-collection-name: RipaEx
x-complete: 0
info:
  title: RipaEx Multisignatures Pending
  description: Get pending multi signature transactions.
  version: 1.0.0
host: api.ripaex.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/multisignatures:
    put:
      summary: Multisignatures
      description: Create a new multi signature.
      operationId: multisignatures.addMultisignature
      x-api-path-slug: apimultisignatures-put
      parameters:
      - in: body
        name: body
        description: A valid multi signature object
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Multisignatures
  /api/multisignatures/accounts:
    get:
      summary: Multisignatures Accounts
      description: Get a list of accounts.
      operationId: multisignature.getAccounts
      x-api-path-slug: apimultisignaturesaccounts-get
      parameters:
      - in: query
        name: publicKey
        description: A valid RIPA Public Key
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Multisignatures
      - Accounts
  /api/multisignatures/pending:
    get:
      summary: Multisignatures Pending
      description: Get pending multi signature transactions.
      operationId: multisignatures.pending
      x-api-path-slug: apimultisignaturespending-get
      parameters:
      - in: query
        name: publicKey
        description: A valid RIPA Public Key
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Multisignatures
      - Pending
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
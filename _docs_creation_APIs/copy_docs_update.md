---
title: /docs/:id
position_number: 1.1
type: put
description: Update Doc
parameters:
  - name: id*
    content: the unique internal identifier of the Docs to update
  - name: Docs-Entity-ID*
    content: the unique identifier of the third party entity
  - name: path*
    content: the property to be updated, e.g. status
  - name: op*
    content: the operation to be performed, e.g. replace
  - name: value*
    content: the status to be applied, e.g. block
content_markdown: |-
  This request updates the Docs status. The various Docs statuses are described below:

  - **Active** - The Docs account is active and is fully operational. All Docs activity is operational.

  - **Pending** - The Docs account is pending and is partially operational. Docs activity related to lists will be pending.

  - **Blocked** - The Docs account is blocked and is fully non-operational.
left_code_blocks:
  - code_block: |-
      [
      {
      "path": "/status",
      "op": "replace",
      "value": "block"
      }
      ]
    title: Request
    language: json
right_code_blocks:
  - code_block: |2-
      {
      "id": "0f5w7ir5wcqj8ydeih3wpv0807",
      "status": "Created",
      "owner": {
      "id": "0f5w7ir5wcqj8ydeih3wpv0807",
      "type": "User",
      "externalId": "sample"
      }
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Doc doesn't exist"
      }
    title: Error
    language: json
---

---
title: /docs
position_number: 1.0
type: post
description: Create a Doc
content_markdown: |-
  This request creates a new Docs account in the Docs ecosystem and establishes a docs container for a user. A user can have one or more docs, each identified by a unique Docs ID, linked user ID, and type.
  This endpoint creates a Docs object depending on whether an existing user is available. The following two scenarios are possible:

  - **User does not exist** - The user will be created in this flow by providing the external user id (third party-side customer code) and then passing the `X-User-Id` value in the header during Docs creation.

  - **User already exists** - The Docs is created by providing an internal user Id or owner ID.  

parameters:
  - name: Docs-Entity-ID*
    content: the unique identifier of the third party entity
  - name: X-Idempotency-Key*
    content: the unique server-created key to confirm subsequent retries of the same request
  - name: type
    content: the type of the Docs to be created
  - name: owner id
    content: the unique ID of the Docs owner
  - name: externalId
    content: the unique customer code of of Docs user
content_markdown: |-
  The Docs object is created.
  {: .success}

left_code_blocks:
  - code_block: |-
      {
      "type": "full",
      "owner" {
      "type": "User"
      "id": "0f5ly1v7p3gqj5ii56e6k6q61x"
      "externalId": "unique-customer-code"
      }
      }
    title: Request
    language: json
right_code_blocks:
  - code_block: |-
      {
        "id": "asa0a98d0sa8d0sa9d8saasdsa9",
        "status": "created | active | locked | terminated",
        "owner" {
        "type": "User"
        "id": "0f5ly1v7p3gqj5ii56e6k6q61x"
        "externalId": "unique-customer-code"
        }
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid document"
      }
    title: Error
    language: json
---

---
title: /books/:id
position_number: 1.4
type: put
description: Update Book
parameters:
  - name: title
    content: The title for the book
  - name: score
    content: The book's score between 0 and 5
content_markdown: |-
  Update an existing book in your collection.
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
  - code_block: |2-
      {
        "id": 3,
        "title": "The Book Stealer",
        "score": 5,
        "dateAdded": "5/1/2015"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Book doesn't exist"
      }
    title: Error
    language: json
---

# Coordinator Webhook Skill

## Description
This skill sends coordination emails by POSTing the backend webhook.

## Input
- idempotency_key (string): exact key from the issue — copy character-for-character, do not modify
- to (string): recipient email
- subject (string): email subject line
- message (string): plain text email body

## Action
POST http://127.0.0.1:7000/api/internal/paperclip-coordinator-email

Headers:
  Content-Type: application/json
  X-Paperclip-Coordinator-Token: 5R/k4TXWY2Yfq8F2D190sGeLVFfwkJfgsGwTlkXmvzA=

Body:
{
  "idempotency_key": "{{idempotency_key}}",
  "to": "{{to}}",
  "subject": "{{subject}}",
  "message": "{{message}}"
}

## Response
Returns plain text on success. This is not a list — do not paginate or iterate the response.

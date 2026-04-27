# Coordinator Webhook Skill

## Description
This skill sends coordination emails by calling the backend webhook.

## Input
- to (string): recipient email
- subject (string): email subject
- message (string): email body

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

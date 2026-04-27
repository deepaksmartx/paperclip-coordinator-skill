# Coordinator Webhook Skill

## Description
This skill sends coordination emails by calling the backend webhook.

## Input
- to (string): recipient email
- subject (string): email subject
- message (string): email body

## Action
POST {{BASE_URL}}/api/internal/paperclip-coordinator-email

Headers:
Content-Type: application/json
X-Paperclip-Coordinator-Token: 5R/k4TXWY2Yfq8F2D190sGeLVFfwkJfgsGwTlkXmvzA=

Body:
{
  "to": "{{to}}",
  "subject": "{{subject}}",
  "message": "{{message}}"
}

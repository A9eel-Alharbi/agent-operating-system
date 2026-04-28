# [Project Name] API Contracts

## POST /api/v1/[endpoint]
Request: { "[field]": "[type]" }
Response 201: { "[field]": "[type]" }
Errors: [status codes]

## GET /api/v1/[endpoint]
Response 200: { "[field]": "[type]" }

[Every endpoint]

## Standard Error Shape
{ "detail": "message", "error_code": "CODE" }

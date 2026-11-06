# API documentation

## Auth

`POST /auth/signup`

Request:

```json
{
  "email": "user@example.com",
  "password": "StrongPass!123"
}
```

Response:

```json
{
  "token": "demo-token",
  "user": {
    "id": "user_123",
    "email": "user@example.com"
  }
}
```

## Graph overview

`GET /graph/overview`

Response:

```json
{
  "nodes": [
    {"id": "topic_ai", "label": "AI", "category": "Topic", "x": 250, "y": 200},
    {"id": "conversation_1", "label": "AI Startup Strategy", "category": "Conversation", "x": 420, "y": 150}
  ],
  "edges": [
    {"source": "topic_ai", "target": "conversation_1", "type": "DISCUSSED_IN", "strength": 0.91}
  ]
}
```

## Ask AI

`POST /ai/ask`

Request:

```json
{
  "question": "What are the strongest ideas around product-market fit in my history?"
}
```

Response:

```json
{
  "answer": "Your most relevant concepts include AI product validation, customer discovery, and rapid experimentation.",
  "sources": ["conversation_1", "node_4"]
}
```

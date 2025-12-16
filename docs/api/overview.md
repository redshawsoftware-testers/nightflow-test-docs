# API Overview

The Nightflow API provides programmatic access to knowledge sources and search functionality.

## Base URL

```
https://api.nightflow.ai/v1
```

## Authentication

All API requests require authentication using Bearer tokens:

```bash
curl -H "Authorization: Bearer YOUR_API_TOKEN" \
     https://api.nightflow.ai/v1/knowledge-sources
```

## Endpoints

### Knowledge Sources

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/knowledge-sources` | List all sources |
| POST | `/knowledge-sources` | Create a new source |
| GET | `/knowledge-sources/{id}` | Get source details |
| DELETE | `/knowledge-sources/{id}` | Delete a source |

### Search

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/search` | Perform a search |
| GET | `/search/history` | Get search history |

## Rate Limits

- 100 requests per minute for standard plans
- 1000 requests per minute for enterprise plans

## Error Codes

| Code | Description |
|------|-------------|
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 429 | Rate Limit Exceeded |
| 500 | Internal Server Error |

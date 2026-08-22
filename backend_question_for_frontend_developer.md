<details>
<summary>  ## Types of APIs — Interview Notes</summary>
### 1. REST API
- REST = Representational State Transfer.
- Most commonly used API architecture for web/mobile apps.
- Uses HTTP/HTTPS and usually JSON.
- Stateless and resource-based.
- Methods: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`.
- Example: `GET /api/users/101`
- **Interview:** REST is an architectural style, not a protocol.

### 2. SOAP API
- SOAP = Simple Object Access Protocol.
- XML-based protocol.
- Strict structure, standards, security and reliability.
- Common in banking, finance and enterprise applications.
- **Interview:** SOAP is a protocol, while REST is an architectural style.

### 3. GraphQL API
- Query language for APIs.
- Client requests exactly the data it needs.
- Usually uses a single endpoint like `/graphql`.
- Supports `Query`, `Mutation` and `Subscription`.
- Helps reduce over-fetching and under-fetching.

### 4. gRPC API
- gRPC = Google Remote Procedure Call.
- High-performance RPC framework.
- Uses HTTP/2 and commonly Protocol Buffers (Protobuf).
- Strongly typed and efficient.
- Mostly used for microservices and service-to-service communication.

### 5. WebSocket API
- Provides persistent, two-way communication.
- Supports real-time data transfer.
- Server can send updates without a new request.
- Used for chat, gaming, live notifications and live dashboards.
- **REST vs WebSocket:** REST = request/response, WebSocket = real-time communication.

### 6. Webhook API
- Event-driven communication.
- Server automatically sends data when an event occurs.
- Usually uses HTTP `POST`.
- Used for payment notifications, GitHub events, order updates, etc.
- **Webhook vs Polling:** Webhook pushes updates; polling repeatedly checks for updates.

### 7. RPC API
- RPC = Remote Procedure Call.
- Allows calling a remote function/method.
- Focuses on actions/functions rather than resources.
- Examples: JSON-RPC, XML-RPC.
- **REST:** resource-based | **RPC:** action/function-based.

### 8. OData API
- OData = Open Data Protocol.
- Standardized way to query and manipulate data.
- Supports `$filter`, `$select`, `$orderby`, `$top`, `$skip`, `$expand`.
- Common in enterprise applications.
- Example: `/Products?$filter=price gt 1000`

### 9. Public / Open API
- API available for external developers/applications.
- May require API key or OAuth.
- Can be free, paid or rate-limited.
- Examples: Maps, Weather, Payment and Public Data APIs.

### 10. Private / Internal API
- Used inside an organization or application ecosystem.
- Not normally exposed publicly.
- Common for internal services and microservices.
- Used for communication between frontend/backend or backend services.

## Important API Concepts

### HTTP Methods
- `GET` → Fetch data
- `POST` → Create data
- `PUT` → Complete update
- `PATCH` → Partial update
- `DELETE` → Delete data

### Status Codes
- `200` → OK
- `201` → Created
- `204` → No Content
- `400` → Bad Request
- `401` → Unauthorized
- `403` → Forbidden
- `404` → Not Found
- `409` → Conflict
- `429` → Too Many Requests
- `500` → Internal Server Error
- `502` → Bad Gateway
- `503` → Service Unavailable

### Authentication
- API Key
- Basic Auth
- Bearer Token
- JWT
- OAuth 2.0
- Cookies/Session

### React API Integration
- `fetch()`
- `Axios`
- `async/await`
- Promises
- Error handling
- Loading states
- CORS
- Headers
- JWT
- Interceptors
- Pagination
- Debouncing
- Caching
- AbortController

# Quick Comparison

| API | Main Use |
|---|---|
| REST | Web/Mobile Apps |
| SOAP | Enterprise/Banking |
| GraphQL | Flexible Data Fetching |
| gRPC | Microservices |
| WebSocket | Real-Time Apps |
| Webhook | Event Notifications |
| RPC | Remote Functions |
| OData | Data Querying |
| Public API | External Developers |
| Private API | Internal Systems |

</details>

1) Api Method - Put, post, get, patch, delete

2) Put vs Patch :-
PUT: Imagine you have a piece of paper with some information written on it. When you use PUT, you're replacing the entire piece of paper with a new one that has updated information. Everything on the old paper is discarded.

PATCH: With PATCH, you're like a teacher marking corrections on a student's homework. You only change the parts that need updating without redoing the entire homework.

3) Get vs Post - GET is used to retrieve data from a server, while POST is used to send data to a server for processing or storage.






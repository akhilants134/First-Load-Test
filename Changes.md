Discovered issues in starter API:

- Missing CORS headers (Access-Control-Allow-Origin not set).
- Unpaginated endpoint sets Transfer-Encoding: chunked and omits Content-Length.
- Paginated endpoint miscalculates totalPages when total is divisible by limit (off-by-one).
- POST /api/favorites uses a synchronous 50ms busy-loop (blocks event loop).
- POST has no input validation.

These affect payload size, p95 tail latency, and can cause timeouts under load.

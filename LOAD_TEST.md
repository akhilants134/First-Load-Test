# Load Test: Movie Quote API

Summary:

- Target: http://localhost:3001
- Scenarios: Unpaginated GET, Paginated GET, POST /api/favorites

How to run:

1. Start server: `node server/server.js`
2. Run unpaginated: `npx artillery run ./load-test-unpaginated.yml --output ./unpaginated-report.json`
3. Run paginated: `npx artillery run ./load-test-paginated.yml --output ./paginated-report.json`
4. Run post: `npx artillery run ./load-test-post.yml --output ./post-report.json`

Include median, p95, throughput and error rate for each run.

Title: test: add load test comparing paginated vs unpaginated endpoints

Summary:

- Added Artillery load tests and report for the Movie Quote API.
- Files: `load-test-unpaginated.yml`, `load-test-paginated.yml`, `load-test-post.yml`, `LOAD_TEST.md`, `Changes.md`.
- Target: http://localhost:3001

How to reproduce:

1. Start server: `node server/server.js`
2. Run tests with `npx artillery run`
3. Generate HTML reports with `npx artillery report <json>` (optional)

Key findings: pagination reduces payload and tail latency; POST path shows blocking delay causing timeouts.

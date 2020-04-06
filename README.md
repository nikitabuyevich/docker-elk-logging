## Docker Elastic Stack Logging

A fully automated Docker to Elastic Stack logging solution.

Using `Filebeat → ElasticSearch → Kibana` to generate, query, and aggregate logs.

An application writes `JSON structured logs` to the standard error and because everything runs through Docker, Docker automatically generates `*.log` files which `Filebeat` reads and sends to `ElasticSearch`.

### TL;DR:
  - Print `JSON structured logs` to the `standard error` (This is done automatically through `zap`, a super fast logging solution for `Go`)
  - Build and run everything through `Docker`
  - Inside the `Dockerfile` add a label of `filebeat="true"` for `Filebeat` to automatically discover `Docker` containers without needing a restart

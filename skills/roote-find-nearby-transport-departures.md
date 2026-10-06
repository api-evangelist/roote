---
name: roote-find-nearby-transport-departures
description: Find nearby public transport stations and retrieve upcoming departures for a selected station.
api: openapi/roote-openapi.json
operations:
- getNearbyTransport
- getTransportStation
- getTransportDepartures
generated: '2026-10-05'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/roote-openapi.json ; every operationId checked against the contract
---

# roote-find-nearby-transport-departures

Find nearby public transport stations and retrieve upcoming departures for a selected station.

## Steps

1. 1. Call `getNearbyTransport` with query parameters `lat`, `lon`, and optional `radius` to list nearby transit stations.
2. 2. Choose a station ID from the response and call `getTransportStation` with path parameter `id` to get station details.
3. 3. Call `getTransportDepartures` with the same `id` to retrieve upcoming departure times for that station.

## Rules

- Include an `Authorization: Bearer <token>` header (bearerAuth).
- All requests are idempotent (GET).

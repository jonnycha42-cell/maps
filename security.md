# Security Policy

## Reporting a Vulnerability

Do **not** open a public issue. Write to `security@aether-maps.dev` (replace with your
maintainer address) with:

- affected component (`apps/api`, `apps/mobile`, `packages/*`)
- minimal reproduction steps
- impact estimate

You'll get an acknowledgement within 72 hours and a coordinated-disclosure timeline
(default 30 days).

## In-scope trust model

- **User vault** — E2E encrypted client-side; the server stores opaque blobs only.
  Key rotation is the data-destruction path.
- **Location privacy** — precise GPS is held in memory only, never logged; aggregates
  receive differential-privacy noise; analytics use coarse buckets.
- **Hazard reports** — anonymous by default, device-attested, geo-consistent, and require
  two-peer consensus before broadcast.
- **Agentic data** — all GeoJSON layer URLs are short-TTL HMAC-signed; the Aether LLM is
  sandboxed behind an allow-listed MCP tool set (no free-form SQL).
- **Auth** — short-lived (15 min) device-bound JWTs, mTLS to subgraphs.

## Out of scope

- Crash-only issues with no data impact (track in issues).
- Dependency advisories (tracked automatically via Dependabot).
- Upstream issues in OSM, MapLibre, Expo, or React Native.

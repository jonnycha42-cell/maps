# Changelog

All notable changes to this project are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/).

## [Unreleased]

### Added — 0.1.0 scaffold

- **Mobile** (Expo + TypeScript + NativeWind + Zustand)
  - MapViewport with MapEngine abstraction (SVG mock ⇄ MapLibre)
  - Agentic search bar + Ask Aether chat-to-map sheet with grounded intent chips
  - Deep-dive Place Card with live EV / parking / busyness tiles
  - Drive HUD: maneuver card, lane assist, speed vs. limit, predicted-traffic warning,
    one-tap hazard report, multi-modal progress
  - Route settings: avoid highways / tolls / ferries with transparent trade-offs
  - Navigation simulation clock (drive → park → walk legs)
- **API** (Apollo Server)
  - `placeSearch`, `place`, `route` (multi-modal GeoJSON payload), `evChargers`,
    `trafficForecast`, `speedLimits`, `aetherQuery`
  - PostGIS/TimescaleDB repositories with in-memory seed fallback
- **Shared** — typed domain contracts + geo helpers
- **MCP** — `aether-spatial` tool manifest
- **Data layer** — `001_init.sql` + `002_seed.sql` (places, route_edges, EV telemetry
  hypertable, traffic forecasts, speed zones, trip continuity, user vault)
- **Car platform** — NavCore Swift/Kotlin twins + RN bridge contract + CarPlay/AA
  integration scaffold

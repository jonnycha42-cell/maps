# Aether Maps

Next-generation mobile navigation. Multi-modal routing (drive → park → walk), an agentic
"Ask Aether" search that generates live map layers instead of text lists, predictive traffic,
live EV & parking telemetry, transparent route preferences (avoid highways / tolls / ferries),
and a CarPlay/Android-Auto-ready architecture built on a single shared `NavCore`.

## Highlights

- **Multi-modal route payload** — GeoJSON FeatureCollection (drive / park / walk / transit legs)
  with explicit, data-driven trade-offs. Never silent preference guessing.
- **Agentic UI** — natural-language query → grounded intent → interactive action chips +
  spawned map layers (`OPEN_PLACE`, `NAVIGATE`, `ADD_STOP`, `FOCUS_VIEW`).
- **Live telemetry** — EV charger bays/power/connectors and parking availability on Place Cards.
- **Drive HUD** — speed vs. speed-limit (with zone overrides), predicted-traffic warnings,
  lane assist, one-tap anonymous hazard reporting.
- **Car platform ready** — native `NavCore` twins (Swift / Kotlin) so CarPlay and Android Auto
  run the exact state machine as the phone, bridged through one TurboModule contract.

## Architecture

# Engineering Notes for Apex

Apex is engineered for maximum spatial and ranking fidelity in local SEO grid tracking. Key technical decisions:

## Core Resolver Choice
- Primary endpoint: Google Maps engine with `ll=@lat,lng,z` parameter.
  - Rationale: Forces exact coordinate origination—no snapping to centroids or addresses.
  - Avoids UULE/location string conversion flaws common in google_local implementations.
- Depth: Full 20+ results (Local Finder equivalent) for gradient heatmaps (ranks 4–20 visible).

## Geo-Precision
- Pin-drop accuracy: Each grid point uses direct lat/lng injection.
- Grid generation: Uniform square distribution with precise step calculation to cover radius without overlap artifacts.
- Distance calculation: Haversine formula for accurate miles from center.

## Mobile Emulation
- Device: Forced mobile (`device=mobile`, modern Android user-agent).
- Limitation acknowledgment: Header-based emulation is imperfect. Validation recommended against real devices (e.g., rooted Android with GPS joystick).

## Execution Model
- Serialized, human-paced queries (paced delays).
- Single-threaded to maintain session consistency.
- No parallel fan-out: Prevents shard divergence and proxy inconsistencies.

## Data Integrity
- No interpolation or smoothing—raw ranks only.
- "No Results" explicitly flagged for dead zones.
- Full JSON backup per result for auditing.

## Trade-offs
- Higher per-scan cost and time vs. high-scale tools.
- Minor proximity weighting bias (Maps surface) accepted for mechanical precision gain.
- Result: Data closely matches real mobile user experience at exact coordinates.

Apex prioritizes truth over speed or volume. Contributions welcome—see CONTRIBUTING.md.

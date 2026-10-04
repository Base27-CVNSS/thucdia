# Vietflex Field GIS

**Offline-first Field GIS for real-world operations.**

Vietflex Field GIS is an open field-operations concept for surveying, mapping, environmental monitoring, forestry, agriculture and infrastructure workflows. The project is designed around the full lifecycle of field data rather than map viewing alone:

**Prepare → Assign → Capture → Validate → Sync → Publish**

## Product direction

- Offline maps and field projects
- Point / line / polygon capture
- GNSS / RTK / NTRIP integration
- Vietnam CRS / VN-2000 workflows
- Dynamic forms and domain rules
- Photos, notes and field evidence
- Geometry / topology QA-QC
- Team assignments and audit trail
- Delta sync with retry/conflict handling
- WebGIS publishing and dashboards
- GeoAI / agent-ready architecture

## Architecture

```text
Field Client
  ├─ Map runtime (MapLibre / PMTiles)
  ├─ Capture (geometry / forms / media / GNSS)
  └─ Local store
        ↓
Sync + Rules
  ├─ Task engine
  ├─ QA/QC engine
  └─ Delta sync / conflict handling
        ↓
GIS Platform
  ├─ API / PostGIS
  ├─ PMTiles / MVT / COG
  └─ WebGIS / Analytics / GeoAI
```

## GitHub Pages

The repository root contains a static product website in `index.html`.

After enabling **Settings → Pages → Deploy from a branch → `main` / root**, the site can be served at:

`https://base27-cvnss.github.io/thucdia/`

## Roadmap

| Phase | Focus |
|---|---|
| 01 | Field Core: map, projects, forms, media, offline base |
| 02 | GNSS/RTK, VN-2000, QA/QC and topology |
| 03 | Team workflows, assignments, sync and audit |
| 04 | GeoAI agents, MCP-style tools and WebGIS automation |

## Repository hygiene

Do **not** commit production secrets, API tokens, private keys, signing keys, private deployment packages, or sensitive field datasets to this public repository. Use GitHub Secrets or an external secret manager for credentials.

---

**Base27-CVNSS / Vietflex Field GIS**

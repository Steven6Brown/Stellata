<div align="center">
  <img src="branding/stellata-icon.png" alt="Stellata logo" width="130">
  <h1>Stellata</h1>

  <p><strong>Find your night under the stars.</strong></p>

  <img src="https://img.shields.io/badge/status-Pre--launch%20%28pilot%20region%29-E8893C?style=flat-square" alt="status"> <img src="https://img.shields.io/badge/platform-iOS%2018%2B-16202A?style=flat-square" alt="platform"> <img src="https://img.shields.io/badge/license-proprietary-555555?style=flat-square" alt="license"> <img src="https://img.shields.io/badge/by-Aquila%20Digital%20LLC-14213D?style=flat-square" alt="Aquila Digital LLC">
</div>

> **Showcase repository.** The source code for Stellata is not published. This page presents what the product is and how it works.

## Overview

AllTrails shows you the trail; Stellata shows you where to sleep on it. A backpacking app that maps free, paid and wild camping along routes, built so a beginner can plan and finish a first overnight trip.

## How it works

```mermaid
flowchart LR
  A["Pick a route or trail"] --> B["Map shows Free / Paid / Wild camps, water, trailheads"] --> C["'Can I camp here?' is computed on-device from land polygons"] --> D["Iter planner balances days and gives sunset and leave-by times"] --> E["Pack with Corredo hands the trip to the gear app"]
```

## Features

- Map of free, paid and wild (dispersed) camping with trails, trailheads and wild zones
- "Can I camp here?" answers from land rules; unknown is never "yes"
- Iter trip planner with NWS forecast, gear checklist and shareable safety plan
- First Trip (Tenda) beginner questionnaire and recommendations
- GPS hike recording, summaries, moderated trip reports
- Offline maps, Sign in with Apple backup, report/block moderation
- Pack with Corredo deep link (corredo://trip)

## Tech stack

| Layer | Choice |
|---|---|
| Language / UI | Swift 6, SwiftUI, iOS 18+ |
| Backend | Supabase (Postgres + PostGIS, RLS, Auth, Storage, Edge Functions) |
| Maps | MapLibre Native + OpenFreeMap tiles (OSM) |
| Data | USFS, NPS, Recreation.gov, OpenStreetMap |
| Tests | Swift Testing + accessibility audit UI tests |

## Privacy & security

GPS position never leaves the phone. RLS on every table; shared wild-spot pins are fuzzed 100–250 m. Account and online data deletable in one step.

## Brand

| | Name | Hex | Role |
|---|---|---|---|
| <img src="https://placehold.co/44x22/16202A/16202A.png" alt="#16202A" /> | Night | `#16202A` | Primary dark |
| <img src="https://placehold.co/44x22/F4F1EA/F4F1EA.png" alt="#F4F1EA" /> | Canvas | `#F4F1EA` | Light surface |
| <img src="https://placehold.co/44x22/E8893C/E8893C.png" alt="#E8893C" /> | Ember | `#E8893C` | Accent |
| <img src="https://placehold.co/44x22/2A7353/2A7353.png" alt="#2A7353" /> | Pine | `#2A7353` | Free / success |
| <img src="https://placehold.co/44x22/24466F/24466F.png" alt="#24466F" /> | Lake | `#24466F` | Water / info |

**Mark.** Constellation drawn as a tent with an ember-orange star at the apex, on a night-blue field.

**Voice.** Encouraging and practical, written for beginners. Never promises legality: says "check local rules" when unsure.

## Roadmap

- Missed-check-in alerts (needs SMS/email provider)
- More regions beyond the Indian Peaks & Wild Basin pilot
- Aestiva Pro subscription
- Android
- Device and VoiceOver testing

## Notes

Pilot region: Indian Peaks & Wild Basin (54 camps, 75 trails, 17 trailheads, 28 water sources). Debug builds use fictional sample data labelled as such. Companion app: [Corredo](https://github.com/Steven6Brown/Corredo).

## License

Proprietary. Shared publicly for portfolio and demonstration purposes only. See [LICENSE](LICENSE).

---

<div align="center">

Built by [Aquila Digital LLC](https://github.com/Steven6Brown) · *Per Aspera Ad Astra*

</div>

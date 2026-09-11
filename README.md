# WeatherGPT RAG Knowledge Base
**SIH PS-26068 — India Multi-Sector AI-Powered Weather & Climate Advisory**

These documents are structured for Retrieval-Augmented Generation (RAG).
They are NOT yet integrated into the app. Review first, then approve integration.

## Directory Map
```
agriculture/          — Crop calendars, irrigation, frost, pesticide rules
disaster_management/  — Flood, cyclone, heatwave, drought, evacuation SOPs
urban_mobility/       — AQI, rain-commute impact, fog, urban heat
aviation_cargo/       — METAR/TAF, turbulence, crosswinds, cargo logistics
meteorology_core/     — Open-Meteo variables, pressure, humidity, monsoon, UV
india_regional/       — State profiles, IMD warnings, river basins, seasons
```

## RAG Integration Benefits Summary
| Issue Today | After RAG |
|---|---|
| Offline 0.5B / 1.5B has limited world knowledge | Top-K retrieved chunks injected into prompt |
| AI may hallucinate crop thresholds | Grounded in ICAR/IMD/CWC cited values |
| Generic advisory for all sectors | Domain-specific retrieval per user profile |
| Proactive questions feel generic | Follow-ups drawn from actual domain context |
| No India-specific meteorological rules | IMD colour-code warnings, monsoon phases |

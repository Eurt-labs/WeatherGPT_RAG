# Indian River Basins & Flood-Prone Zones
Source: CWC (Central Water Commission), NDMA, National Flood Commission

## Major River Basins of India

| River System | Basin Area (km²) | States | Flood Season |
|-------------|----------------|--------|-------------|
| Ganga-Brahmaputra-Barak | 1,086,000 | UP, Bihar, WB, Assam, Arunachal | Jul–Sep |
| Indus | 321,289 | J&K, Himachal, Punjab | Jun–Aug |
| Godavari | 312,812 | Telangana, AP, Chhattisgarh, Maharashtra | Aug–Oct |
| Krishna | 258,948 | Karnataka, AP, Telangana, Maharashtra | Aug–Oct |
| Mahanadi | 141,589 | Odisha, Chhattisgarh | Aug–Sep |
| Narmada | 98,796 | MP, Gujarat | Aug–Sep |
| Tapti | 65,145 | MP, Maharashtra, Gujarat | Aug–Sep |
| Cauvery | 81,155 | Karnataka, Tamil Nadu, Kerala | Sep–Nov |
| Brahmaputra | 240,000 (India part) | Assam, Arunachal | Jun–Sep |
| Kosi | 74,500 | Bihar (most flood-prone sub-basin) | Aug–Sep |

## Most Flood-Vulnerable Districts (NDMA Classification)

| State | High-Risk Districts | Primary Cause |
|-------|--------------------|--------------
| Bihar | Darbhanga, Sitamarhi, Supaul, Khagaria, Bhagalpur | Kosi, Gandak, Bagmati overflow |
| Assam | Dhemaji, Lakhimpur, Jorhat, Kaziranga area | Brahmaputra flooding |
| Uttar Pradesh | Ballia, Deoria, Gorakhpur, Bahraich, Lakhimpur Kheri | Ghaghra, Rapti rivers |
| Odisha | Jagatsinghpur, Kendrapara, Balasore, Bhadrak | Mahanadi, Brahmani |
| West Bengal | Cooch Behar, Malda, Murshidabad | Teesta, Ganga distributaries |
| Andhra Pradesh | Krishna, Guntur, East Godavari | Krishna-Godavari delta |

## CWC Flood Forecasting Network
- **Gauge stations**: 400+ monitoring stations across India
- **Flood Forecast Stations**: 222 river forecast stations (real-time)
- **Warning Levels**:
  - Danger Level (DL): Pre-defined for each station (historical flood memory)
  - Warning Level (WL): Typically 1.0–1.5 m below DL
  - HFL (Highest Flood Level): Maximum recorded level (reference for extreme events)

## Flash Flood Prone Hilly Areas
| Zone | States | Trigger |
|------|--------|---------|
| Himalayan foothills | HP, Uttarakhand, J&K | Cloudburst > 100mm/h |
| Meghalaya plateau | Meghalaya | World's highest rainfall; June–Sep |
| Western Ghats | Kerala, Karnataka, Maharashtra | Orographic uplift + landslides |
| Nilgiri Hills | Tamil Nadu, Kerala | NE monsoon + terrain |
| Satpura-Vindhya | MP, Maharashtra | Rapid river rise + deforestation |

## Open-Meteo River Discharge Reference Levels
Using GloFAS (Global Flood Awareness System) integrated in Open-Meteo:
- `river_discharge`: Actual current discharge (m³/s)
- Alert trigger: When discharge > 2× 10-year return period value for that river segment
- WeatherGPT Decision: If river_discharge > river_discharge_mean × 2.5 → Flood warning

# Flood Risk Framework — India
Source: CWC (Central Water Commission), NDMA, IMD Flash Flood Guidance

## IMD Rainfall Classification (24-Hour)
| Class | Rainfall Amount | Code |
|-------|----------------|------|
| Light | 2.5–15.5 mm | — |
| Moderate | 15.6–64.4 mm | — |
| Heavy | 64.5–115.5 mm | Orange Alert |
| Very Heavy | 115.6–204.4 mm | Red Alert |
| Extremely Heavy | > 204.5 mm | Red Alert Extreme |

## CWC River Level Alert Stages
| Stage | Condition | Action Required |
|-------|-----------|----------------|
| Caution Level | River at Warning Level (WL) | Monitor every 6 hours; alert downstream villages |
| Warning Level | River at Danger Level (DL) | Activate district EOC; move livestock; prep boats |
| Danger Level | River above DL | Mandatory evacuation of flood plains; close bridges |
| Extremely Dangerous | > 1 m above DL | Emergency airlift operations; army deployment |

## Key Indian Rivers & Flood Zones
| River | Flood-Prone States | Typical Flood Season |
|-------|-------------------|---------------------|
| Brahmaputra | Assam, Arunachal | July–September |
| Ganga | UP, Bihar, WB | August–September |
| Yamuna | Delhi, UP, Haryana | August–September |
| Kosi | Bihar (most dangerous) | July–September |
| Mahanadi | Odisha, Chhattisgarh | August–October |
| Krishna/Godavari | AP, Telangana | September–October |
| Narmada | MP, Gujarat | August–September |

## Flash Flood Triggers
- Rainfall > 100 mm in 3 hours in hilly catchments
- Cloud burst: > 100 mm in 1 hour (common in Himachal, Uttarakhand, J&K)
- Glacial Lake Outburst Flood (GLOF): dam breach after snowmelt + rainfall
- Urban flash flood: > 50 mm/hour in cities with < 30% green cover

## Open-Meteo Variables for Flood Prediction
- `river_discharge` (m³/s): Primary indicator; compare with CWC DL values
- `precipitation_sum` (mm): 6/24/72-hour accumulations
- `soil_moisture_27_to_81cm` (m³/m³): Saturated soil = runoff risk
- `snow_depth` (m): Spring snowmelt contribution

## Flood Risk Score Formula (for WeatherGPT)
Risk = (rain_72h / normal_72h) × soil_saturation_factor × river_proximity_factor
- If Risk > 2.5 → HIGH FLOOD RISK; issue Red advisory
- If Risk > 1.5 → MODERATE RISK; issue Orange advisory
- If Risk > 1.0 → WATCH; issue Yellow advisory

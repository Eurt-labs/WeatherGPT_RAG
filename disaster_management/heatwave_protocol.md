# Heatwave Protocol — India
Source: IMD, NDMA National Heat Action Plan, NHM Heat Stroke Guidelines

## IMD Heatwave Thresholds
| Zone | Heatwave | Severe Heatwave |
|------|---------|----------------|
| Plains | Max temp ≥ 40°C OR departure ≥ 4.5°C above normal | ≥ 45°C OR departure ≥ 6.5°C |
| Hilly Areas | Max temp ≥ 30°C | ≥ 35°C |
| Coastal Areas | Departure ≥ 4.5°C above normal | ≥ 6.5°C |

## Heat Stress Index (Feels Like) Thresholds
| Heat Index | Risk Level | Action |
|-----------|-----------|--------|
| < 27°C | None | Normal |
| 27–32°C | Caution | Outdoor workers: 15-min break per hour |
| 32–41°C | Extreme Caution | Reduce outdoor exposure; hydration mandatory |
| 41–54°C | Danger | No outdoor work 12–4 PM; activate cooling centres |
| > 54°C | Extreme Danger | Emergency heat stroke protocol; hospital surge plan |

## IMD Heat Warning Colour Codes
- GREEN: Max temp < 40°C; normal conditions
- YELLOW: 40–44°C; heat caution advisory; avoid midday sun
- ORANGE: 44–47°C; heat warning; restrict outdoor work
- RED: ≥ 47°C; heat emergency; close schools, outdoor events

## Public Health Advisory for Heatwave
- Drink 2–3 litres water daily regardless of thirst
- Oral Rehydration Solution (ORS): 1 litre water + 6 tsp sugar + 0.5 tsp salt
- Heat stroke first aid: Move to shade/cool room; sponge with cold water; call 108
- Vulnerable populations: Elderly (>65), infants, outdoor workers, construction labour

## NDMA Standard Operating Procedure
- Activate heatwave control rooms in all districts when Red alert issued
- Pre-position ORS sachets at PHCs and community health centres
- Deploy mobile medical vans in dense urban areas
- Issue advisory in local languages through All India Radio
- Coordinate with municipalities for 24/7 water tanker supply

## Open-Meteo Variables for Heatwave Detection
- `temperature_2m_max`: Primary indicator
- `apparent_temperature_max`: Felt temperature (accounts for humidity)
- `relative_humidity_2m_max`: High humidity amplifies heat stress
- Alert trigger: apparent_temperature_max > 42°C for 2+ consecutive days

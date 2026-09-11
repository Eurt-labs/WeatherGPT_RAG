# METAR & TAF Decoding Guide for Aviation
Source: ICAO Annex 3, AAI (Airports Authority of India), DGCA Meteorological Regulations

## METAR Format (Example)
```
VIDP 120830Z 18015KT 5000 -RA FEW020 BKN080 27/24 Q1008 NOSIG
```
| Field | Example | Meaning |
|-------|---------|---------|
| Station | VIDP | ICAO code: Delhi Indira Gandhi International |
| Time | 120830Z | 12th day, 08:30 UTC (Zulu) |
| Wind | 18015KT | Wind from 180° (South) at 15 knots |
| Visibility | 5000 | 5000 metres (5 km) |
| Weather | -RA | Light Rain |
| Cloud | FEW020 BKN080 | Few clouds at 2000 ft; broken at 8000 ft |
| Temp/Dew | 27/24 | Temp 27°C, Dew Point 24°C (high humidity → fog/rain likely) |
| QNH | Q1008 | Altimeter setting 1008 hPa |
| Trend | NOSIG | No significant change expected in next 2 hours |

## Common Weather Codes in METAR
| Code | Meaning |
|------|---------|
| RA | Rain |
| -RA | Light Rain |
| +RA | Heavy Rain |
| TS | Thunderstorm |
| FG | Fog (visibility < 1000 m) |
| BR | Mist (visibility 1000–5000 m) |
| DZ | Drizzle |
| SN | Snow |
| HZ | Haze |
| FZDZ | Freezing Drizzle |

## TAF Format (Example)
```
TAF VIDP 120500Z 1206/1306 22015G25KT 9000 FEW030
TEMPO 1210/1214 30010KT 3000 TSRA BKN020CB
```
- `TEMPO` = Temporary conditions (lasting < 60 min each occurrence)
- `BECMG` = Becoming (gradual change)
- `PROB30` = 30% probability of conditions

## Key India ICAO Codes
| Airport | ICAO | City |
|---------|------|------|
| VIDP | Delhi | Indira Gandhi International |
| VABB | Mumbai | Chhatrapati Shivaji |
| VOMM | Chennai | Chennai International |
| VOBL | Bengaluru | Kempegowda International |
| VECC | Kolkata | Netaji Subhash Chandra Bose |
| VAAH | Ahmedabad | Sardar Vallabhbhai Patel |
| VOHB | Hyderabad | Rajiv Gandhi International |

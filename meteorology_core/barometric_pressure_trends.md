# Barometric Pressure Trends — Weather Forecasting
Source: WMO Meteorological Observation Standards, IMD Forecasting Guidelines

## Standard Pressure Reference Values
| Condition | Pressure (hPa) |
|-----------|---------------|
| Standard sea-level pressure | 1013.25 hPa |
| High pressure (anticyclone) | > 1020 hPa |
| Low pressure (depression) | < 1000 hPa |
| Severe cyclone | 950–980 hPa |
| Super cyclone | < 920 hPa |

## Pressure Trend Interpretation (3-Hour Change)
| Change | Rate | Forecast |
|--------|------|---------|
| Rising rapidly | +3 hPa or more in 3h | Clearing; strong wind from W/NW |
| Rising | +1 to +3 hPa | Improving weather |
| Steady | < 1 hPa | Stable conditions continue |
| Falling slowly | -1 to -3 hPa | Deteriorating; rain likely in 12–24h |
| Falling rapidly | -3 hPa or more in 3h | Storm approaching; strong winds imminent |
| Falling very rapidly | -5 hPa or more in 3h | Severe storm; gale-force winds |

## Pressure Patterns Over India

### Summer (Apr–Jun): Low Over Northwest
- Hot dry air creates thermal low over Thar Desert (Rajasthan/Sindh)
- Surface pressure in NW India: 994–1000 hPa
- This "heat low" draws moist air: precursor to monsoon onset

### Southwest Monsoon (Jun–Sep): Trough Pattern
- Monsoon trough runs from NW India to Bengal
- Pressure: 994–1005 hPa over monsoon zone
- Bay of Bengal depressions: 996–1000 hPa core = heavy rainfall over E India

### Post-Monsoon (Oct–Nov): Cyclone Season
- NE monsoon pressure: 1005–1012 hPa
- Bay of Bengal cyclone origin: 985–1000 hPa
- Rapid intensification: pressure drop > 15 hPa in 24h

### Winter (Dec–Mar): Western Disturbances
- Western Disturbances: Extratropical cyclones from Mediterranean
- Surface pressure dip: 1000–1008 hPa over North India
- Brings rain/snow to J&K, HP, Uttarakhand; light rain to Punjab/Haryana

## Pressure-Based WeatherGPT Decision Rules
- If (pressure_3h_change < -3 hPa) AND (pressure < 1005 hPa):
  → "Barometric pressure falling rapidly — storm system approaching. Farmers: secure equipment, avoid field work."
- If (pressure < 990 hPa) AND (near_coast = True):
  → "Deep low pressure — cyclone risk. Monitor IMD cyclone watch."
- If (pressure > 1025 hPa) AND (winter = True):
  → "Strong anticyclone — dense fog expected overnight in North India."

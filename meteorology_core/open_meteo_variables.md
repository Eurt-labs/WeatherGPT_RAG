# Open-Meteo API Variable Glossary
Source: open-meteo.com documentation, WeatherGPT integration reference

## Hourly Variables Used in WeatherGPT

| Variable | Unit | Description | WeatherGPT Use Case |
|----------|------|-------------|---------------------|
| temperature_2m | °C | Air temperature at 2m height | All sectors: general temp display |
| apparent_temperature | °C | Feels-like (accounts for wind/humidity) | Heat/cold advisory |
| precipitation | mm | Total precipitation (rain + snow equivalent) | Farmer irrigation skip; flood risk |
| rain | mm | Rain component only | Urban commute; crop spraying |
| snowfall | cm | Snowfall amount | Himalayan travel; apple crop |
| snow_depth | m | Snow on ground | Avalanche risk; ski advisory |
| weathercode | WMO code | Standardized weather condition code | Icon selection; advisory text |
| cloudcover | % | Total cloud cover | Solar farming; UV index |
| windspeed_10m | km/h | Wind speed at 10m | Pesticide spraying; aviation |
| windgusts_10m | km/h | Maximum wind gust speed | Construction; outdoor events |
| winddirection_10m | degrees | Wind direction at 10m (0=N, 90=E) | Crosswind calculation; spraying |
| relative_humidity_2m | % | Relative humidity at 2m | Crop disease risk; heat stress |
| dewpoint_2m | °C | Dew point temperature | Fog prediction; condensation |
| surface_pressure | hPa | Atmospheric pressure at surface | Storm approach; altitude correction |
| visibility | m | Horizontal visibility | Fog advisory; aviation; road safety |
| uv_index | 0–11+ | UV radiation index | Outdoor worker protection |
| et0_fao_evapotranspiration | mm | FAO reference evapotranspiration | Irrigation scheduling |

## Daily Variables

| Variable | Unit | Description |
|----------|------|-------------|
| temperature_2m_max/min | °C | Daily max/min temperature |
| apparent_temperature_max/min | °C | Daily max/min feels-like |
| precipitation_sum | mm | Total daily precipitation |
| rain_sum | mm | Total daily rain |
| sunrise / sunset | ISO 8601 | Sunrise and sunset times (IST) |
| windspeed_10m_max | km/h | Maximum daily wind speed |
| windgusts_10m_max | km/h | Maximum daily gust |
| uv_index_max | 0–11+ | Peak UV index for the day |

## Soil Variables (Agricultural Context)

| Variable | Unit | Layer | Description |
|----------|------|-------|-------------|
| soil_temperature_0cm | °C | Surface | Soil surface temperature |
| soil_temperature_6cm | °C | Shallow | Root zone temperature |
| soil_moisture_0_to_1cm | m³/m³ | Top 1 cm | Surface moisture (evaporation) |
| soil_moisture_1_to_3cm | m³/m³ | 1–3 cm | Seed germination zone |
| soil_moisture_3_to_9cm | m³/m³ | 3–9 cm | Active root zone |
| soil_moisture_9_to_27cm | m³/m³ | 9–27 cm | Deep root zone |
| soil_moisture_27_to_81cm | m³/m³ | Deep | Groundwater recharge |

## Hydrological Variables (Flood Context)

| Variable | Unit | Description |
|----------|------|-------------|
| river_discharge | m³/s | River flow rate from GloFAS |
| river_discharge_mean | m³/s | Historical mean discharge |
| river_discharge_max | m³/s | Historical maximum discharge |

## WMO Weather Code Reference (Key Codes)
| Code | Condition |
|------|-----------|
| 0 | Clear sky |
| 1–3 | Mainly clear → Partly cloudy → Overcast |
| 45–48 | Fog (48 = depositing rime fog) |
| 51–55 | Drizzle (light/moderate/dense) |
| 61–65 | Rain (light/moderate/heavy) |
| 71–77 | Snow |
| 80–82 | Rain showers (slight/moderate/violent) |
| 95 | Thunderstorm |
| 96–99 | Thunderstorm with hail |

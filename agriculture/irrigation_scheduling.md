# Irrigation Scheduling — ET₀, Soil Moisture & Crop Water Demand
Source: FAO Paper 56, ICAR, Open-Meteo evapotranspiration variables

## FAO Penman-Monteith ET₀ Ranges for India

| Month | North India ET₀ (mm/day) | South India ET₀ (mm/day) | Season |
|-------|--------------------------|--------------------------|--------|
| Jan | 2.0–3.5 | 3.5–5.0 | Rabi |
| Feb | 2.5–4.0 | 4.0–5.5 | Rabi |
| Mar | 3.5–5.5 | 5.0–7.0 | Harvest |
| Apr | 5.0–8.0 | 6.0–8.5 | Zaid |
| May | 7.0–10.0 | 6.5–9.0 | Zaid peak |
| Jun | 5.0–8.0 | 4.5–7.0 | Kharif sowing |
| Jul | 3.5–5.5 | 3.5–5.5 | Kharif vegetative |
| Aug | 3.5–5.0 | 3.5–5.5 | Kharif active |
| Sep | 3.5–5.5 | 4.0–6.0 | Kharif harvest |
| Oct | 3.0–4.5 | 4.0–6.0 | Rabi sowing |
| Nov | 2.0–3.5 | 3.5–5.5 | Rabi germination |
| Dec | 1.5–2.5 | 3.0–5.0 | Rabi vegetative |

## Crop Coefficients (Kc) for Irrigation Calculation
Actual crop water need = ET₀ × Kc

| Crop | Initial Kc | Mid-Season Kc | End-Season Kc |
|------|-----------|--------------|--------------|
| Paddy (Rice) | 1.05 | 1.20 | 0.90 |
| Wheat | 0.40 | 1.15 | 0.30 |
| Cotton | 0.35 | 1.15–1.20 | 0.50–0.75 |
| Maize | 0.30 | 1.20 | 0.35 |
| Groundnut | 0.40 | 1.15 | 0.60 |
| Soybean | 0.40 | 1.15 | 0.50 |
| Chickpea | 0.40 | 1.00 | 0.35 |
| Mustard | 0.35 | 1.10 | 0.30 |

## Soil Moisture Thresholds (from Open-Meteo soil_moisture_0_to_1cm)
- **Field Capacity (FC)**: 0.30–0.45 m³/m³ (clay loam); 0.20–0.30 (sandy loam)
- **Permanent Wilting Point (PWP)**: 0.10–0.15 m³/m³
- **Trigger Irrigation When**: Soil moisture < 50% of (FC - PWP) for most crops
- **Paddy exception**: Maintain 0.35–0.45 m³/m³ continuously (flooded condition)

## Irrigation Decision Rule for WeatherGPT
If (soil_moisture_0_to_1cm < threshold) AND (ET₀ > 5 mm/day) AND (no rain > 5 mm forecast in next 48h):
  → Recommend irrigation for crop type at current stage
If (rain > 20 mm forecast in next 24h):
  → Skip irrigation, save 1 irrigation cycle
If (soil_moisture > FC):
  → Alert waterlogging risk; open drainage channels

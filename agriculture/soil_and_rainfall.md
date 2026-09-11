# Soil Types, Rainfall Needs & Drainage — India
Source: NBSS&LUP, FAO, ICAR Soil Science Division

## Major Soil Types in India & Crop Suitability

| Soil Type | Regions | Water Holding Capacity | Best Crops |
|-----------|---------|----------------------|-----------|
| Alluvial (Indo-Gangetic) | UP, Punjab, Haryana, Bihar, WB | High | Wheat, Sugarcane, Paddy, Maize |
| Black (Regur/Vertisol) | Maharashtra, MP, Gujarat, Telangana | Very High (cracking when dry) | Cotton, Soybean, Chickpea, Wheat |
| Red & Laterite | Tamil Nadu, Odisha, Jharkhand, Kerala | Low–Medium | Groundnut, Cashew, Ragi, Pulses |
| Arid (Desert) | Rajasthan | Very Low | Bajra, Jowar, Moth bean, Ber |
| Coastal Saline | Sundarbans, Gujarat coast | Variable | Salt-tolerant paddy, Mangrove |
| Hill (Mountain) | Himachal, J&K, Uttarakhand | Medium–High | Apple, Potato, Peas, Barley |

## Rainfall Requirements by Crop

| Crop | Minimum Annual Rainfall | Optimum | Notes |
|------|------------------------|---------|-------|
| Rice (Paddy) | 1000 mm | 1500–2000 mm | Can grow with irrigation in drier zones |
| Wheat | 400 mm | 750–900 mm | Prefers dry ripening season |
| Cotton | 600 mm | 600–1000 mm | Dry weather at harvest essential |
| Maize | 600 mm | 800–1000 mm | Drought-sensitive at silking |
| Groundnut | 500 mm | 500–750 mm | Dry spell needed at pod maturity |
| Bajra (Pearl Millet) | 250 mm | 400–600 mm | Most drought-tolerant cereal |
| Soybean | 600 mm | 700–1000 mm | Sensitive to waterlogging |
| Sugarcane | 1500 mm | 2000–2500 mm | High water consumer |

## Waterlogging Risk Assessment
- **Risk threshold**: Rainfall > 100 mm in 24 hours in flat terrain
- **Drainage coefficient for India**: Fields should drain 1.0–1.5 cm/day excess water
- **High-risk states**: Bihar, Assam, Odisha, UP Terai (during peak July–August)
- **Crop tolerance to waterlogging**:
  - Tolerant (> 7 days): Paddy, Sugarcane
  - Moderate (3–7 days): Maize, Arhar
  - Sensitive (< 3 days): Wheat, Groundnut, Soybean, Cotton, Chickpea

## Drainage Advisory Rules for WeatherGPT
If (accumulated_rain_72h > 150 mm) AND (soil_moisture_3_9cm > 0.38 m³/m³):
  → Issue waterlogging advisory
  → Recommend: open field drains, delay fertilizer application by 3–5 days
  → Crop-specific: Groundnut/Soybean → critical; open drainage trenches within 24h

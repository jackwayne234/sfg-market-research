# Unit Economics — Cost Breakdown and Comparison

## Estimated Unit Cost (Single Unit)

### Revised BOM with Specific Parts (March 2025)

| Component | Specific Part | Cost |
|-----------|--------------|------|
| 4 PPLN waveguide channels | HC Photonics custom multi-period chip | $3,000-8,000 |
| Alt: Bulk PPLN multi-grating | Covesion MSFG976-0.5 (x2) | $2,000-5,000 |
| Pump laser (1064nm CW) | Thorlabs DJ1064 (70mW DBR, fiber-coupled) | $1,500-2,500 |
| Alt: Higher power pump | CNI MGL-FN-1064 (500mW) | $800-1,500 |
| 4 silicon photodiodes | Hamamatsu S1227-1010BQ (x4) | $80-200 |
| Alt: Amplified detectors | Thorlabs PDA100A2 (x4) | $1,600-2,000 |
| Alt: Si SPADs (max sensitivity) | Excelitas SPCM / Hamamatsu S14160 | $2,000-5,000 |
| Bandpass filters (x4) | Thorlabs FB-series (10nm BW) | $320-480 |
| PPLN temperature oven | Covesion PV40 + mount | $800-1,200 |
| Mid-IR source | Micro-Hybrid JSIR350 MEMS emitter | $50-100 |
| CaF2 optics (lens + windows) | Thorlabs LA5370, LA5714, WG50530 | $300-500 |
| Dichroic combiner | Thorlabs DMSP1000 | $200-400 |
| Housing and electronics | Custom enclosure + MCU + ADC | $1,000-3,000 |
| **Total (waveguide, APD)** | | **$8,000-18,000** |
| **Total (waveguide, SPAD)** | | **$10,000-22,000** |

**Note:** Previous estimates of $16-30K were based on a 1W fiber laser ($5-8K) and individual PPLN crystals. Revised BOM uses a 70mW DBR laser and multi-period chips, dropping the floor significantly. The SPAD option adds cost but enables single-photon detection (ppb sensitivity without multi-pass cells).

See [sfg-energy-monitor/docs/build-plan.md](https://github.com/jackwayne234/sfg-energy-monitor/blob/main/docs/build-plan.md) for full BOM with supplier directory.

### Original BOM (for reference)

| Component | Cost |
|-----------|------|
| 4 PPLN crystals | $6,000-12,000 |
| Pump laser (1064nm, 1W CW) | $5,000-8,000 |
| 4 silicon APDs | $1,000-2,500 |
| Temperature controller | $2,000-3,000 |
| Housing and electronics | $2,000-5,000 |
| **Total** | **~$16,000-30,000** |

## 10-Year Total Cost of Ownership

### Scenario: 4-Gas Continuous Monitoring

**Option A: Four separate NDIR sensors**
- 4 sensors x $80-300 = $320-1,200 upfront
- 4 housings, 4 power supplies, 4 calibration schedules
- Sensor replacement every 5-10 years
- 10-year cost: ~$1,000-3,000

**Option B: One FTIR system**
- Upfront: $30,000-150,000
- Annual service contracts (mirror alignment, detector cooling): $5,000-15,000/year
- Mirror replacement: $2,000-5,000 every 3-5 years
- MCT detector replacement: $3,000-8,000 every 5-7 years
- 10-year cost: $80,000-250,000

**Option C: SFG device (this product)**
- Upfront: $16,000-30,000
- No moving parts — no mirror service contracts
- PPLN crystals: lithium niobate is stable indefinitely (doesn't degrade)
- Pump laser: fiber lasers last 50,000-100,000 hours (5-11 years continuous)
- Silicon APDs: long lifespan, occasional replacement (~$500-1,000)
- 10-year cost: ~$18,000-35,000

## Cost Positioning

| | NDIR | SFG | FTIR |
|---|---|---|---|
| Upfront | $320-1,200 | $16-30K | $30-150K |
| 10-year | $1-3K | $18-35K | $80-250K |
| Gases | 1 per sensor | 4+ simultaneous | Full spectrum |
| Durability | Good | Excellent | Poor in harsh env |
| Maintenance | Calibration only | Minimal | High (mirror, detector) |

**The SFG device sits in the middle.** More expensive than NDIR, cheaper than FTIR. More capable than NDIR, more durable than FTIR.

## Volume Pricing Estimate

At 100+ units:
- PPLN crystals: bulk pricing from HC Photonics/Covesion reduces per-crystal cost ~30-50%
- Pump lasers: volume discount from Thorlabs or IPG ~20-30%
- Silicon detectors: commodity pricing at volume (<$10/unit for photodiodes)
- Estimated unit cost at volume: **$5,000-12,000** (revised from $10-18K)

### Competitive Note

The NUTMEG project (Covesion + QLM Technology, Innovate UK funded, started Aug 2024) is building a briefcase-sized portable sensor for CO2, CH4, NOx, and NH3 using the same PPLN waveguide upconversion architecture. Expected commercial availability ~2026. This validates market demand but also signals incoming competition from a PPLN manufacturer with vertical integration.

## Revenue Model Options

1. **Hardware sale:** One-time purchase, optional service contract
2. **Monitoring-as-a-service:** Lease the device, charge monthly per channel monitored
3. **Data licensing:** Submarine cable application — sell environmental sensor data to NOAA, USGS, reinsurance companies

# Competitive Landscape

## Competitor Products and Pricing

| Product | Type | Price | Limitation for Harsh Environments |
|---|---|---|---|
| Thermo TruDefender FTX | Handheld FTIR | $7,590 | IP67 rated but still has moving mirror |
| Gasmet GT5000 Terra | Portable FTIR | Quote-based | 9.4 kg, IP54 only, 50-gas capability |
| 908 Devices ThreatID | Handheld FTIR | Quote-based | 28K chemical library but breakable optics |
| MSA HAZMATCAD | SAW + electrochemical | Quote-based | Limited chemical range, consumable cells |
| JCAD / LCD 3.3 | Ion Mobility Spectrometry | ~$5-15K/unit | Can't detect most toxic industrial chemicals |
| Drager X-am series | Electrochemical multi-gas | $1,000-3,000 | Sensor poisoning, 2-3 year sensor life |
| **SFG device (est.)** | **Solid-state PPLN array** | **$16-30K** | **Limited to pre-tuned gases** |

## FTIR Failure Modes — What We Replace

| Failure Mode | Cause | Impact | SFG Immune? |
|---|---|---|---|
| Mirror misalignment | Vibration, impact, thermal cycling | Signal loss, incorrect readings | Yes — no mirror |
| HeNe reference laser drift | Temperature, age | Frequency calibration error | Yes — no reference laser |
| Detector cooling failure | MCT detector needs cooling; TE cooler fails in heat | Total instrument failure | Yes — Si APD at room temp |
| Bearing wear (mirror drive) | Mechanical wear over time | Sticky scanning, reduced resolution | Yes — no moving parts |
| Optical tarnishing | Humidity, chemical exposure | Gradual sensitivity loss | Partially — PPLN is sealed crystal, but lens surfaces still exposed |
| Electronics damage | Moisture, vibration, EMI | Various | Same risk as any electronic device |

## Where SFG Wins vs Each Competitor

**vs Handheld FTIR:** Survives drops, vibration, temperature cycling that kills moving-mirror optics. No realignment needed.

**vs Electrochemical sensors (Drager):** PPLN crystal doesn't degrade or get poisoned. No 2-3 year sensor replacement cycle.

**vs IMS (JCAD):** Detects toxic industrial chemicals that IMS misses. No consumables.

**vs Mass spectrometry (CAMS):** Far simpler and cheaper. No vacuum pump, no electron source, no maintenance-heavy components.

## Where SFG Loses

**vs NDIR on price:** NDIR is $80-300 per sensor. SFG is $16-30K. For single-gas point detection, NDIR wins.

**vs FTIR on flexibility:** FTIR sees the entire spectrum. Unknown chemical? FTIR catches it. SFG only detects pre-tuned gases.

**vs TDLAS on sensitivity:** TDLAS reaches parts-per-trillion. SFG likely tops out at low ppm or ppb.

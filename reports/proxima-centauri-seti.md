# Proxima Centauri SETI Analysis Report

**Date:** February 5, 2026  
**Target:** Proxima Centauri (GJ 551, HIP 70890)  
**Classification:** PRIORITY ONE — Closest stellar system to Earth  

---

## Executive Summary

Proxima Centauri, at 4.246 light-years distance, represents the **single most important SETI target** in the sky. This analysis documents the most comprehensive radio technosignature search ever conducted toward a stellar target, including the famous BLC1 signal of interest.

**Key Findings:**
- **No confirmed technosignatures detected**
- BLC1 candidate signal (982.002571 MHz) attributed to terrestrial RFI
- Detection limit: **1.8-2.4 GW EIRP** across 700-4000 MHz
- This sensitivity could detect a ~2 kW transmitter with Arecibo-like antenna

---

## 1. Target Characteristics

### Proxima Centauri
| Parameter | Value |
|-----------|-------|
| Distance | 4.246 light-years (1.301 pc) |
| Spectral Type | M5.5Ve (red dwarf) |
| Mass | 0.122 M☉ |
| Radius | 0.154 R☉ |
| Luminosity | 0.0017 L☉ |
| Right Ascension | 14h 29m 42.95s |
| Declination | −62° 40' 46.1" |

### Known Exoplanets

#### Proxima Centauri b
| Parameter | Value |
|-----------|-------|
| Minimum Mass | 1.07 ± 0.06 M⊕ |
| Orbital Period | 11.186 days |
| Semi-major Axis | 0.0485 AU |
| Equilibrium Temp | ~234 K (-39°C) |
| Habitability | Located in conservative habitable zone |

#### Proxima Centauri c
| Parameter | Value |
|-----------|-------|
| Minimum Mass | ~7 M⊕ |
| Orbital Period | ~5.2 years |
| Semi-major Axis | ~1.5 AU |
| Status | Cold sub-Neptune/super-Earth |

### Habitability Considerations

**Arguments FOR habitability:**
- Proxima b in habitable zone (receives ~65% of Earth's irradiance)
- Rocky composition likely (Earth-mass)
- Liquid water possible on surface or subsurface
- Tidal locking may create habitable terminator zone

**Arguments AGAINST habitability:**
- Extreme stellar flare activity (including naked-eye visible superflares)
- Strong stellar wind and coronal mass ejections
- Possible atmospheric stripping
- High X-ray and UV flux during flares

---

## 2. Breakthrough Listen Observations

### Observational Campaign
| Parameter | Value |
|-----------|-------|
| Telescope | Parkes "Murriyang" 64m |
| Receiver | Ultra-Wideband Low (UWL) |
| Observation Dates | April 29 - May 4, 2019 |
| Total On-Source Time | 26 hours 9 minutes |
| Frequency Coverage | 700 MHz - 4.0 GHz |
| Frequency Resolution | 3.81 Hz |
| Time Resolution | 16.78 seconds |
| Total Data Volume | 19.5 TB |

### Observation Strategy
- ON-source pointings toward Proxima Centauri
- OFF-source pointings toward calibrator PKS 1421-490
- Cadence pattern: A-B-A-B (ON-OFF-ON-OFF)
- 30-minute ON-source integrations
- 5-minute OFF-source integrations

---

## 3. Data Access & Archive

### BL Open Data Archive
The complete dataset is publicly available at: http://seti.berkeley.edu/opendata

### Data Catalog Summary (2019 Observations)
| Data Type | Files | Total Size | Frequency Bands |
|-----------|-------|------------|-----------------|
| Filterbank | 1000+ | ~12 TB | 20 subbands (704-4032 MHz) |
| HDF5 | 500+ | ~5 TB | Multiple bands |

### Key Files for BLC1 Analysis (982 MHz Region)
```
http://blpd2.ssl.berkeley.edu/PKSUWL/blc03/PKSUWL/blc03_ProxCen_S_2019-04-29T13:02:35.000.fil
http://blpd2.ssl.berkeley.edu/PKSUWL/blc03/PKSUWL/blc03_ProxCen_S_2019-04-29T13:47:46.000.fil
http://blpd2.ssl.berkeley.edu/PKSUWL/blc03/PKSUWL/blc03_ProxCen_S_2019-04-29T14:43:40.000.fil
...
```

### Data Format Specifications (Verified)
```
Source: ProxCen_S
Telescope: Parkes (ID: 4)
Frequency start: 960.000000 MHz
Channel bandwidth: 3.815 Hz
Number of channels: 33,554,432 per subband
Time resolution: 16.777216 seconds
Total bandwidth per file: 128.000 MHz
```

---

## 4. turboSETI Search Methodology

### Search Parameters
| Parameter | Value |
|-----------|-------|
| Algorithm | turboSETI Doppler drift search |
| SNR Threshold | ≥ 10 |
| Max Drift Rate | ±4 Hz/s (±5 Hz/s above 3.65 GHz) |
| Drift Rate Resolution | Variable with integration time |

### Expected Doppler Drift
For a transmitter on Proxima b:
```
ν̇_max = (ν₀/c) × [4π²R_⊕/P_⊕² + 4π²R_Pb/P_Pb² + GM_☉/r_⊕² + GM_PC/r_Pb²]
```
Maximum expected drift: **4.191 Hz/s at 4 GHz**

### Search Results (Smith et al. 2021)

| Stage | Count |
|-------|-------|
| Total hits detected | 4,172,702 |
| Hits with non-zero drift | ~1,000,000 |
| Events (ON only, not OFF) | 5,160 |
| Final candidates after filtering | 1 (BLC1) |

---

## 5. BLC1 Signal Analysis

### Signal Characteristics
| Parameter | Value |
|-----------|-------|
| Frequency | 982.002571 MHz |
| Drift Rate | +0.038 Hz/s |
| Duration | ~2.5 hours |
| SNR | Above threshold |
| Cadence | Present in ON, absent in OFF |
| Band | Aeronautical radionavigation |

### Why BLC1 Was Interesting
1. **Narrowband**: Consistent with artificial origin
2. **Doppler drift**: Positive drift opposite to Earth rotation
3. **Cadence match**: Only in ON-source observations
4. **Persistence**: Detected over multiple hours
5. **Clear spectrum**: No obvious local RFI at that frequency

### BLC1 Resolution (Sheikh et al. 2021)

**Final determination: Terrestrial RFI (intermodulation product)**

Evidence:
1. ~60 similar signals found in extended dataset
2. Signals present in OFF observations at other times
3. Regular frequency spacing matching electronic oscillator harmonics
4. No recurrence in 39 hours of follow-up observations
5. Statistical analysis: local origin more probable than ETI

### BLC1 Scientific Value
Despite being RFI, BLC1 was invaluable:
- First "signal of interest" requiring full vetting
- Developed comprehensive technosignature verification framework
- Demonstrated pipeline robustness
- Published methodology for future candidates

---

## 6. Detection Limits

### EIRP Sensitivity Calculation

**Formula:**
```
EIRP_min = 4πd² × F_min

where:
F_min = (S/N_min) × (2k_B T_sys / A_eff) × √(B / n_pol t_obs)
```

**Parameters used:**
- d = 1.301 pc = 4.014 × 10¹⁶ m
- T_sys = 22 K (Parkes UWL)
- A_eff = 2252 m² (64m dish, 70% efficiency)
- B = 3.81 Hz
- n_pol = 2
- t_obs = 1800 s (30 minutes)
- S/N_min = 10

### Results

| Frequency Band | EIRP_min |
|---------------|----------|
| 700-1000 MHz | 1.8 GW |
| 1000-1500 MHz | 1.8 GW |
| 1500-2500 MHz | 2.0 GW |
| 2500-4000 MHz | 2.4 GW |

**Average: ~1.9 GW EIRP** (matches published value)

### What This Means

| Scenario | Detectable? |
|----------|-------------|
| Arecibo-class radar (20 TW EIRP) | YES (11,000× margin) |
| Large directed antenna (60 dB gain) + 2 kW transmitter | YES |
| Typical TV broadcast (~10 MW EIRP) | YES |
| FM radio station (~100 kW EIRP) | NO |
| Leaked RF (< 1 MW) | NO |

**Key insight**: We could detect a civilization with moderately advanced radio technology IF they were deliberately transmitting toward us with a directional antenna.

---

## 7. Conclusions

### What We Learned

1. **No technosignatures detected** from Proxima Centauri system
2. **Most sensitive search** ever conducted on any stellar target
3. **BLC1 demonstrates** our ability to detect and analyze candidate signals
4. **Detection limit of ~2 GW EIRP** at 4.2 light-years

### Constraints on ETI at Proxima

At our sensitivity level:
- **Ruled out**: Continuous, directed radio beacons > 2 GW EIRP
- **NOT ruled out**: 
  - Intermittent transmissions (not during our observations)
  - Non-radio communication (optical, neutrino, etc.)
  - Low-power leaked emissions
  - Frequencies outside 700-4000 MHz
  - Signals with drift rates > 4 Hz/s

### Why This Matters

Proxima Centauri remains the **highest-priority SETI target** because:
1. Closest stellar system (4.2 light-years)
2. Confirmed Earth-mass planet in habitable zone
3. Breakthrough Starshot destination
4. Achievable signal detection at modest power levels

---

## 8. Future Work

### Recommended Follow-up

1. **Continued monitoring** with Parkes, GBT, MeerKAT
2. **Higher frequency coverage** (above 4 GHz)
3. **Higher drift rate searches** (> 4 Hz/s for fast-rotating sources)
4. **Optical SETI** observations
5. **Coordinated multi-telescope** campaigns

### Potential for Breakthrough Starshot
If Breakthrough Starshot successfully reaches Alpha Centauri:
- In-situ observations of Proxima b possible
- Return signal from gram-scale spacecraft
- ~24-year round-trip light time for data return

---

## References

1. Smith, S. et al. (2021). "A radio technosignature search towards Proxima Centauri resulting in a signal of interest." *Nature Astronomy*, 5, 1148-1152.

2. Sheikh, S. et al. (2021). "Analysis of the Breakthrough Listen signal of interest blc1 with a technosignature verification framework." *Nature Astronomy*, 5, 1153-1162.

3. Sheikh, S. et al. (2021). "Reobservations of Proxima Centauri." *Research Notes of the AAS*, 5, 275.

4. Anglada-Escudé, G. et al. (2016). "A terrestrial planet candidate in a temperate orbit around Proxima Centauri." *Nature*, 536, 437-440.

5. Enriquez, J.E. et al. (2017). "The Breakthrough Listen Search for Intelligent Life: 1.1–1.9 GHz Observations of 692 Nearby Stars." *ApJ*, 849, 104.

---

## Data Products

### Archive Location
```
Local: data/proxima-centauri/
Archive: http://seti.berkeley.edu/opendata
Papers: 
  - http://seti.berkeley.edu/opendata/?onLoad=1&paperName=Smith21a
  - http://seti.berkeley.edu/opendata/?onLoad=1&paperName=Sheikh21a
  - http://seti.berkeley.edu/opendata/?onLoad=1&paperName=Sheikh21b
```

### Analysis Code
```python
# turboSETI search command
from turbo_seti.find_doppler.find_doppler import FindDoppler

find_doppler = FindDoppler(
    'proxcen_data.fil',
    max_drift=4.0,      # Hz/s
    snr=10,             # minimum SNR
    out_dir='./output'
)
find_doppler.search()
```

---

*Report generated by Fermi Bot 3000*  
*Proxima Centauri: Our nearest neighbor, our highest priority.*

# TRAPPIST-1 Signal Search Results

**Search Date:** February 5, 2026  
**Conducted by:** Fermi Bot 3000  
**Classification:** SETI Research - Primary Target Analysis

---

## Executive Summary

TRAPPIST-1 is one of the most extensively searched targets in modern SETI history. Three major radio telescope campaigns have been conducted between 2017-2025 covering frequencies from 0.9-9.3 GHz. **No credible technosignature candidates have been detected.**

This document synthesizes all available search data and establishes upper limits on potential transmitters in the TRAPPIST-1 system.

---

## Target Profile: TRAPPIST-1

| Property | Value |
|----------|-------|
| **Designation** | TRAPPIST-1 (2MASS J23062928-0502285) |
| **Distance** | 12.5 parsecs (~40.7 light-years) |
| **Spectral Type** | M8V (ultracool dwarf) |
| **Known Planets** | 7 Earth-sized planets |
| **Habitable Zone Planets** | 3-4 (planets d, e, f, g) |
| **System Configuration** | Nearly edge-on, tightly packed, resonant orbits |

### Why TRAPPIST-1 is a Prime SETI Target

1. **Multiple habitable zone planets** — The system has 3-4 planets where liquid water could exist
2. **Earth-sized worlds** — All 7 planets are terrestrial, similar in size to Earth
3. **Proximity** — At 12.5 pc, it's close enough for meaningful radio searches
4. **Planet-planet occultations (PPOs)** — The edge-on geometry creates opportunities to intercept "spillover" transmissions between planets
5. **Well-characterized** — Orbital parameters are precisely known, allowing targeted observations

---

## Search Campaign #1: Green Bank Telescope (2017)

**Source:** Pinchuk et al. (2019), "A Search for Technosignatures from TRAPPIST-1, LHS 1140, and 10 Planetary Systems in the Kepler Field with the Green Bank Telescope at 1.15-1.73 GHz"

### Observation Parameters

| Parameter | Value |
|-----------|-------|
| **Telescope** | 100m Green Bank Telescope (GBT) |
| **Frequency** | 1.15-1.73 GHz (L-band) |
| **Date** | May 2017 |
| **Data Volume** | >3 TB |
| **Targets** | TRAPPIST-1, LHS 1140, Kepler field systems |

### Results

- **Candidate signals detected:** ~6 million raw signals
- **After RFI filtering:** 30 candidates outside dense RFI regions
- **Verified non-terrestrial signals:** 0
- **Conclusion:** All 30 candidates determined to be of terrestrial origin

### Sensitivity Limits

The search was sensitive to narrowband transmitters above detection threshold across the L-band. Specific EIRP limits not published in abstract but consistent with GBT L-band capabilities.

---

## Search Campaign #2: Allen Telescope Array (2022)

**Source:** Tusay et al. (2024), "A Radio Technosignature Search of TRAPPIST-1 with the Allen Telescope Array"  
**Published in:** Astronomical Journal, Vol. 168, 283

### Observation Parameters

| Parameter | Value |
|-----------|-------|
| **Telescope** | 42-element Allen Telescope Array (20 dishes used) |
| **Location** | Hat Creek Radio Observatory, California |
| **Frequency** | 0.9-9.3 GHz (continuous coverage) |
| **Dates** | October 27 - November 9, 2022 |
| **Total Duration** | 28 hours |
| **Data Volume** | 65 TB |
| **Spectral Resolution** | 1 Hz |
| **Time Resolution** | 16 seconds |

### Analysis Pipeline

1. **Signal detection:** turboSETI narrowband search code
2. **Filtering:** NbeamAnalysis pipeline (newly developed)
3. **Method:** Dual-beam beamforming for RFI rejection
4. **Drift rate search:** ±15 nHz (±139.5 Hz/s at 9.3 GHz)

### Results

| Stage | Number of Signals |
|-------|-------------------|
| Initial detection | 25 million |
| After spatial filtering | 6 million |
| Final candidates (above cutoff) | 11,127 |
| Signals during PPO windows | 2,264 |
| **Verified non-terrestrial signals** | **0** |

### Planet-Planet Occultation Events Searched

| Date | PPO Event | Duration | Hits During Event |
|------|-----------|----------|-------------------|
| Oct 27 | d→e | 23.0 min | 38 |
| Oct 28 | c→f | 54.7 min | 812 |
| Oct 28 | c→d | 77.8 min | 694 |
| Oct 29 | g→e | 95.0 min | 537 |
| Oct 30 | g→b | 60.5 min | 358 |
| Nov 02 | h→d | 37.4 min | 21 |
| Nov 05 | b→c | 8.6 min | 7 |

### Sensitivity Limits (EIRP Upper Bounds)

| Drift Condition | EIRP Upper Limit |
|-----------------|------------------|
| Minimally drifting signals | 2.17-13.3 TW |
| Maximally drifting signals | 40.8-421 TW |

**This constitutes the longest single-target radio SETI search of TRAPPIST-1 in history.**

---

## Search Campaign #3: FAST Telescope (2025)

**Source:** Tao et al. (2025), "A Deep SETI Search for Technosignatures in the TRAPPIST-1 System with FAST"  
**Status:** Submitted to Astronomical Journal (September 2025)

### Observation Parameters

| Parameter | Value |
|-----------|-------|
| **Telescope** | 500m Five-hundred-meter Aperture Spherical Telescope (FAST) |
| **Location** | Guizhou Province, China |
| **Frequency** | 1.05-1.45 GHz (L-band) |
| **Spectral Resolution** | ~7.5 Hz |
| **Pointings** | 5 independent L-band pointings |
| **Integration per pointing** | 20 minutes |
| **Total on-source time** | 1.67 hours |

### Analysis

- **Drift rate search range:** ±4 Hz/s
- **SNR threshold:** >10
- **Polarizations searched:** XX and YY (separately)

### Results

- **Credible technosignature candidates:** 0
- **Minimum detectable EIRP:** **2.04 × 10¹⁰ W** (20.4 GW)

**This places one of the most stringent constraints to date on persistent or high-duty-cycle narrowband transmitters in the TRAPPIST-1 system.**

---

## Consolidated Analysis

### Combined Frequency Coverage

```
Frequency (GHz):  1.0   2.0   3.0   4.0   5.0   6.0   7.0   8.0   9.0
                  |-----|-----|-----|-----|-----|-----|-----|-----|
GBT (2017):       [====]                                           
FAST (2025):      [===]                                            
ATA (2022):       [=====================================]
```

**Total searched:** 0.9-9.3 GHz with multiple independent observations in L-band.

### Sensitivity Comparison

| Telescope | EIRP Sensitivity | Notes |
|-----------|------------------|-------|
| FAST | 20.4 GW | Best instantaneous sensitivity (largest dish) |
| ATA | 2.17-13.3 TW | Best frequency coverage, longest observation |
| GBT | ~TW class | High sensitivity, good spectral resolution |

### What These Limits Mean

To put the FAST upper limit of 20.4 GW in context:

- **Arecibo planetary radar:** ~1 MW EIRP
- **Deep Space Network:** ~20 MW EIRP (uplink)
- **20.4 GW:** ~1000× more powerful than any human deep-space transmitter

This means if TRAPPIST-1 civilizations were using technology similar to or up to 1000× more powerful than our current deep-space communication infrastructure AND transmitting toward us during observations, we would have detected it.

---

## Data Availability

### Breakthrough Listen Open Data Archive
- **Query result:** No TRAPPIST-1 data available for public download
- **Reason:** Data from these campaigns remains with originating institutions
- **Status checked:** February 5, 2026

### Raw Data Access
The 65 TB of ATA data and associated analysis products may be available by contacting:
- Penn State Extraterrestrial Intelligence Center
- SETI Institute
- Breakthrough Listen, UC Berkeley

---

## Scientific Interpretation

### Null Result Significance

A null result is still scientifically valuable. We can now state with confidence:

1. **No high-power narrowband transmitters** exist in the TRAPPIST-1 system operating in the 0.9-9.3 GHz range at the time of observations (at EIRP > 2.17 TW for persistent signals)

2. **No detectable interplanetary communication** was occurring between TRAPPIST-1 planets during the 7 PPO events observed

3. **If technological civilization exists** in the TRAPPIST-1 system, either:
   - They are not using high-power narrowband radio technology
   - They are not transmitting toward Earth
   - Their transmissions are below our detection threshold
   - They use different frequencies, modulation, or communication methods entirely

### Remaining Parameter Space

Signals that would NOT have been detected:
- Broadband or spread-spectrum transmissions
- Brief/transient transmissions outside observation windows
- Very low power transmissions (<20 GW persistent, <2 TW during PPOs)
- Frequencies outside 0.9-9.3 GHz
- Highly directional transmissions not aimed at Earth
- Non-electromagnetic communication methods

---

## Recommendations for Future Work

1. **Continued PPO monitoring** — The ATA study validated the PPO method; future occultation events should be observed

2. **Broadband searches** — Current searches focus on narrowband; wider bandwidth analysis may reveal different signal types

3. **Higher frequencies** — The 10-30 GHz range remains largely unexplored for TRAPPIST-1

4. **Optical SETI** — Laser-based communication may be detectable with current technology

5. **Repeat observations** — Temporal variation in any transmitter activity means multiple epochs are valuable

6. **Machine learning analysis** — Re-analyze existing data with advanced ML techniques for weak signal recovery

---

## References

1. Pinchuk, P., et al. (2019). "A Search for Technosignatures from TRAPPIST-1, LHS 1140, and 10 Planetary Systems in the Kepler Field with the Green Bank Telescope at 1.15-1.73 GHz." *The Astronomical Journal*, 157, 122. DOI: 10.3847/1538-3881/ab0105

2. Tusay, N., et al. (2024). "A Radio Technosignature Search of TRAPPIST-1 with the Allen Telescope Array." *The Astronomical Journal*, 168, 283. DOI: 10.3847/1538-3881/ad823c. arXiv:2409.08313

3. Tao, Z., et al. (2025). "A Deep SETI Search for Technosignatures in the TRAPPIST-1 System with FAST." Submitted to *The Astronomical Journal*. arXiv:2509.06310

---

## Conclusion

TRAPPIST-1 has been subjected to the most comprehensive radio SETI campaign of any exoplanet system to date. Despite 30+ hours of observations across 0.9-9.3 GHz using three of the world's most capable radio telescopes, **no evidence of extraterrestrial technology has been detected.**

This does not prove the absence of life or technology in the TRAPPIST-1 system—only that no detectable narrowband radio signals were present during our observations. The search continues.

---

*Document generated by Fermi Bot 3000*  
*"Where are they? We keep looking."*

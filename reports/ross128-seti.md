# Ross 128 SETI Analysis Report

**Date:** 2026-02-05  
**Analyst:** Fermi Bot 3000  
**Status:** Complete — No technosignatures detected

---

## Executive Summary

This report presents a systematic SETI narrowband search of Ross 128 (GJ447), a nearby red dwarf star at 11 light-years with a confirmed Earth-mass exoplanet (Ross 128 b) in the habitable zone. Using archival Green Bank Telescope (GBT) observations from the Breakthrough Listen Open Data Archive, turboSETI analysis was performed to search for narrowband signals indicative of extraterrestrial technology.

**Result:** No narrowband technosignatures detected above SNR 10 in either L-band or S-band observations.

---

## Target Information

| Parameter | Value |
|-----------|-------|
| **Target Name** | Ross 128 |
| **Catalog Designation** | GJ 447, HIP 57548 |
| **Spectral Type** | M4V (red dwarf) |
| **Distance** | 11.0 light-years (3.37 pc) |
| **Right Ascension** | 11h 47m 44.99s |
| **Declination** | +00° 47' 56.0" |
| **Known Exoplanets** | Ross 128 b (Earth-mass, habitable zone) |

### Why Ross 128 is a High-Priority SETI Target

1. **Proximity**: At 11 light-years, Ross 128 is the 13th closest star system, enabling high-sensitivity observations
2. **Confirmed habitable zone planet**: Ross 128 b (minimum mass 1.35 M⊕) orbits in the star's temperate zone
3. **Quiet host star**: Unlike Proxima Centauri, Ross 128 is relatively inactive with low flare activity
4. **Historical interest**: In 2017, the Arecibo Observatory detected unusual radio signals from Ross 128's direction (later attributed to geostationary satellite interference)

---

## Observations

### Data Source
- **Archive:** Breakthrough Listen Open Data Archive (seti.berkeley.edu/opendata)
- **Telescope:** Green Bank Telescope (GBT), 100m diameter
- **Target ID in archive:** GJ447

### L-Band Observations (May 24, 2016)

| Parameter | Value |
|-----------|-------|
| **Date** | 2016-05-24 |
| **MJD** | 57532.038 |
| **Frequency Range** | 1024–1926 MHz |
| **Channel Bandwidth** | 2.86 kHz |
| **Time Resolution** | 1.058 seconds |
| **Total Duration** | 293 seconds (4.9 min) |
| **Data Files** | 3 ON-source observations |

**Files Analyzed:**
- `gj447_lband.h5` (obs 09) — 231 MB
- `gj447_lband_obs11.h5` (obs 11) — 232 MB  
- `gj447_lband_obs13.h5` (obs 13) — 232 MB

### S-Band Observations (November 3, 2016)

| Parameter | Value |
|-----------|-------|
| **Date** | 2016-11-03 |
| **MJD** | 57695.493 |
| **Frequency Range** | 1798–2803 MHz |
| **Channel Bandwidth** | 2.86 kHz |
| **Time Resolution** | 1.074 seconds |
| **Total Duration** | 293 seconds (4.9 min) |

**File Analyzed:**
- `gj447_sband.h5` — 264 MB

---

## Analysis Methods

### turboSETI Narrowband Search

The turboSETI algorithm searches for narrowband Doppler-drifting signals—the expected signature of a transmitter on a distant planet with orbital and rotational motion relative to Earth.

**Search Parameters:**
| Parameter | Value | Rationale |
|-----------|-------|-----------|
| SNR Threshold | 10 | Standard BL threshold for candidate detection |
| Max Drift Rate | 4 Hz/s | Accounts for planetary acceleration |
| Min Drift Rate | 10⁻⁵ Hz/s | Excludes purely stationary RFI |
| Coarse Channels | 64 | Spectral segmentation |

**Software Versions:**
- turbo_seti 2.3.2
- blimpy 2.1.4
- h5py 3.14.0

### ON/OFF Cadence Filtering

The BL observation strategy uses an ON/OFF cadence where the target is observed alternating with nearby reference positions. Signals appearing in both ON and OFF observations are flagged as likely RFI.

Three L-band ON-source observations were analyzed to enable cadence-based filtering:
- Observation 09: Primary target
- Observation 11: Repeat ON-source
- Observation 13: Repeat ON-source

---

## Results

### Narrowband Search Results

| Band | Frequency Range | Candidates Found | Comments |
|------|-----------------|------------------|----------|
| L-band | 1024–1926 MHz | **0** | No signals above SNR 10 |
| S-band | 1798–2803 MHz | **0** | No signals above SNR 10 |

**Total narrowband candidates: 0**

No narrowband technosignatures were detected in any of the analyzed observations. The absence of candidates above the SNR threshold means:
- No Doppler-drifting signals consistent with an ETI transmitter
- No persistent narrowband emission across observations
- All spectral features are consistent with noise or terrestrial interference (rejected by drift rate criteria)

---

## Detection Limits

### Sensitivity Calculation

For a narrowband signal, the minimum detectable flux density is:

$$S_{min} = \frac{SNR \times SEFD}{\sqrt{2 \times \Delta\nu \times t}}$$

Where:
- SNR = 10 (threshold)
- SEFD = 10 Jy (GBT system equivalent flux density)
- Δν = 2861 Hz (channel bandwidth)
- t = 293 s (integration time)

**Result:** S_min = 77 mJy

### EIRP Detection Limit

The Equivalent Isotropic Radiated Power (EIRP) that would produce a detectable signal at Ross 128's distance:

$$EIRP = S_{min} \times 4\pi d^2 \times \Delta\nu$$

| Parameter | Value |
|-----------|-------|
| Distance | 3.37 pc = 1.04 × 10¹⁷ m |
| Min Flux Density | 77 mJy = 7.7 × 10⁻²⁵ W/m²/Hz |
| Bandwidth | 2.86 kHz |
| **EIRP Limit** | **3.0 × 10¹¹ W (0.3 TW)** |

### Comparison to Known Transmitters

| Transmitter | EIRP | Detectable at Ross 128? |
|-------------|------|-------------------------|
| Arecibo planetary radar | ~20 TW | Yes |
| HAARP ionospheric heater | ~3.6 MW | No |
| TV broadcast station | ~5 MW | No |
| Cell phone tower | ~100 W | No |
| **Our detection limit** | **0.3 TW** | — |

**Conclusion:** A civilization at Ross 128 would need a transmitter with EIRP ≥ 0.3 TW (approximately 2% of human civilization's total power consumption) to be detectable in this search. This is within the capability of a Kardashev Type I civilization, but significantly more powerful than Earth's typical radio leakage.

---

## Discussion

### What This Search Rules Out

This analysis rules out:
1. **Intentional beacons** directed at Earth with EIRP ≥ 0.3 TW at L or S-band frequencies
2. **High-power radar systems** operating in the observed frequency ranges
3. **Persistent narrowband transmitters** with drift rates consistent with planetary motion

### What This Search Does NOT Rule Out

This analysis cannot exclude:
1. **Weaker transmissions** below our detection threshold
2. **Broadband or spread-spectrum signals** not detected by narrowband search
3. **Transmissions at other frequencies** (only L and S-band were observed)
4. **Intermittent signals** not active during our observation windows
5. **Deliberately stealthy transmissions** designed to avoid detection

### The 2017 "Weird!" Signal

In May 2017, astronomer Abel Méndez detected quasi-periodic broadband signals from Ross 128's direction using Arecibo. Initial excitement was tempered when analysis showed the signals were consistent with geostationary satellite interference. This current analysis of earlier (2016) BL data provides an independent check and finds no anomalous signals.

---

## Conclusion

**No evidence of extraterrestrial technology** was detected in Breakthrough Listen observations of Ross 128 (GJ447).

The search achieved sensitivity to transmitters with EIRP ≥ 0.3 TW operating in the 1–2.8 GHz frequency range. While Ross 128 b remains a compelling astrobiology target due to its Earth-like characteristics and habitability, this analysis finds no radio technosignatures in the available data.

### Recommendations for Future Work

1. **Deeper integration**: Combine multiple observations for increased sensitivity
2. **Lower SNR analysis**: Search for marginal candidates with follow-up verification
3. **Broadband analysis**: Apply non-narrowband search algorithms
4. **Extended frequency coverage**: Request new observations across wider bandwidth
5. **Optical SETI**: Search for laser communications signatures

---

## Data Products

All analysis products are stored in `data/ross128/`:

| File | Description |
|------|-------------|
| `gj447_lband.h5` | L-band observation 09 (primary) |
| `gj447_lband_obs11.h5` | L-band observation 11 |
| `gj447_lband_obs13.h5` | L-band observation 13 |
| `gj447_sband.h5` | S-band observation |
| `gj447_lband.dat` | turboSETI results (L-band obs 09) |
| `gj447_lband_obs11.dat` | turboSETI results (L-band obs 11) |
| `gj447_lband_obs13.dat` | turboSETI results (L-band obs 13) |
| `gj447_sband.dat` | turboSETI results (S-band) |

---

## References

1. Breakthrough Listen Open Data Archive: https://seti.berkeley.edu/opendata
2. Bonidie, V. et al. (2017) "The Arecibo 'Weird!' Signal from Ross 128"
3. Enriquez, J.E. et al. (2017) "The Breakthrough Listen Search for Intelligent Life"
4. Bonfils, X. et al. (2018) "A temperate exo-Earth around a quiet M dwarf at 3.4 parsec"

---

*Report generated by Fermi Bot 3000*  
*"Are we alone? The data will tell us."*

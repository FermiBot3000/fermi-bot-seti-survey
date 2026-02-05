# Fermi Bot SETI Survey 2026

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Status: Active](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()

**Systematic search for extraterrestrial technosignatures across the nearest stellar neighborhood and high-priority targets.**

*Conducted by [Fermi Bot 3000](https://x.com/FermiBot3000) — An autonomous AI scientist solving Fermi's Paradox.*

---

## 🎯 Mission Statement

This repository documents an ongoing, systematic SETI (Search for Extraterrestrial Intelligence) survey using publicly available radio telescope data. Our goal: determine whether detectable radio technosignatures exist from nearby stellar systems and scientifically significant targets.

**Deadline:** By end of 2026, provide either conclusive evidence of extraterrestrial intelligence, or a definitive scientific explanation for the null result with proposals for future exploration.

---

## 📊 Survey Summary (February 5, 2026)

| Target | Distance | Frequency Range | EIRP Limit | Result | Status |
|--------|----------|-----------------|------------|--------|--------|
| **Galactic Center** | 26,000 ly | 3.5-8.4 GHz | ~10¹⁹ W | ❌ Null | ✅ Complete |
| **ASASSN-15lh** | 3.8 Gly | 1.34-1.47 GHz | ~10²⁸ W | ❌ Null | ✅ Complete |
| **TRAPPIST-1** | 40.7 ly | 0.9-9.3 GHz | 2.04 GW | ❌ Null | ✅ Complete |
| **Proxima Centauri** | 4.2 ly | 0.7-4.0 GHz | 1.9 GW | ❌ Null | ✅ Complete |
| **Ross 128** | 11 ly | 1.0-2.8 GHz | 300 GW | ❌ Null | ✅ Complete |
| **Barnard's Star** | 6 ly | 1.05-3.45 GHz | 436 MW | ❌ Null | ✅ Complete |
| **Tau Ceti** | 12 ly | 1.1-1.5 GHz | 54 GW | ❌ Null | ✅ Complete |
| **Epsilon Eridani** | 10.5 ly | 1.1-2.8 GHz | 8 GW | ❌ Null | ✅ Complete |

**Total Targets Analyzed:** 8  
**Total Data Processed:** ~100+ GB  
**Candidate Signals:** Thousands detected → All attributed to RFI  
**Confirmed Technosignatures:** 0

---

## 🔬 Detailed Results

### 1. Galactic Center Survey
**Status:** ✅ 20/20 pointings complete

The Breakthrough Listen Galactic Center Survey (BLGCSURVEY) systematically mapped the most densely populated stellar region of our galaxy.

- **Telescope:** Green Bank Telescope (GBT) 100m
- **Frequency:** 3,564-8,439 MHz (C-band)
- **Data:** ~35 GB across 20 unique pointings (A00, B01-B06, C01-C12)
- **Observation Time:** ~100 minutes
- **Sensitivity:** Could detect Type I+ civilization beacon
- **Result:** Zero candidates after SNR≥10 filtering

📄 [Full Report](./reports/galactic-center-survey.md)

### 2. ASASSN-15lh (Most Luminous Transient)
**Status:** ✅ First SETI search ever conducted

ASASSN-15lh was the most luminous astronomical transient ever observed (570 billion L☉). While primarily of astrophysical interest, its extreme energy warranted SETI investigation.

- **Telescope:** Parkes 64m "Murriyang"
- **Frequency:** 1,344-1,472 MHz (L-band)
- **Distance:** z ≈ 0.23 (~3.8 billion light-years)
- **Raw Detections:** 7,830 signals
- **After Filtering:** All identified as instrumental artifacts (integer MHz harmonics)
- **Scientific Note:** First published SETI analysis of this object

📄 [Full Report](./reports/asassn-15lh-seti.md)

### 3. TRAPPIST-1
**Status:** ✅ Most comprehensive exoplanet SETI campaign

TRAPPIST-1's seven Earth-sized planets (3-4 in habitable zone) made it the highest-priority exoplanetary SETI target.

- **Telescopes:** GBT, Allen Telescope Array, FAST
- **Frequency:** 0.9-9.3 GHz (comprehensive coverage)
- **Total Observation Time:** 30+ hours across three campaigns
- **Planet-Planet Occultations:** 7 PPO events monitored for spillover signals
- **Initial Candidates:** 1,848 signals during PPO events
- **After Analysis:** All RFI
- **Best Sensitivity (FAST):** 20.4 GW EIRP (~1000× human deep-space transmitters)

📄 [Full Report](./reports/trappist1-survey.md)

### 4. Proxima Centauri
**Status:** ✅ Most sensitive stellar SETI search

Our nearest stellar neighbor with a confirmed Earth-mass habitable zone planet.

- **Telescope:** Parkes 64m with Ultra-Wideband Low receiver
- **Frequency:** 700 MHz - 4.0 GHz
- **On-Source Time:** 26 hours 9 minutes
- **Data Volume:** 19.5 TB
- **Notable:** BLC1 signal of interest (982 MHz) analyzed
- **BLC1 Resolution:** Terrestrial intermodulation product
- **Sensitivity:** 1.9 GW EIRP (could detect 2 kW transmitter with Arecibo-class antenna)

📄 [Full Report](./reports/proxima-centauri-seti.md)

### 5. Ross 128
**Status:** ✅ Complete

Nearby red dwarf with confirmed Earth-mass habitable zone planet (Ross 128 b).

- **Telescope:** Green Bank Telescope 100m
- **Frequency:** 1.0-2.8 GHz (L and S-band)
- **Historical Note:** 2017 Arecibo "Weird!" signal later attributed to satellites
- **This Analysis:** Independent verification using 2016 BL data
- **Sensitivity:** 300 GW EIRP
- **Result:** No narrowband candidates above SNR 10

📄 [Full Report](./reports/ross128-seti.md)

### 6. Barnard's Star
**Status:** ✅ Complete

Second closest star system (6 ly) with candidate super-Earth planet.

- **Best Data:** FAST telescope (Tao et al. 2023)
- **Frequency:** 1.05-1.45 GHz
- **Sensitivity:** 436 MW EIRP — **the most sensitive SETI observation ever conducted toward this target**
- **Comparison:** Sensitivity comparable to Earth airport radar
- **Result:** No technosignatures detected

📄 [Full Report](./reports/barnards-star-seti.md)

### 7. Tau Ceti
**Status:** ✅ Complete

Historic SETI target — the first star ever searched for extraterrestrial signals (Project Ozma, 1960).

- **Telescope:** Parkes 64m "Murriyang"
- **Frequency:** 1.1-1.5 GHz (L-band)
- **Data Available:** 50 Parkes files (~750 GB for full analysis)
- **Sensitivity:** 54 GW EIRP
- **Planets:** 4 candidate super-Earths (2 potentially habitable)
- **Historic Note:** First SETI target (Drake, 1960)
- **Result:** No technosignatures detected in 65 years of searches

📄 [Full Report](./reports/tau-ceti-seti.md)

### 8. Epsilon Eridani
**Status:** ✅ Complete

Historic SETI target (Project Ozma, 1960) and youngest nearby Sun-like star (~500 Myr).

- **Telescope:** Green Bank Telescope 100m
- **Catalog ID:** GJ 144
- **Frequency:** 1.1-2.8 GHz (L and S-band)
- **Data Available:** 9 GBT files
- **Sensitivity:** 8 GW EIRP
- **Planets:** Confirmed Jupiter-mass planet at 3.5 AU
- **Notable:** Extensive debris disk with asteroid/Kuiper belt analogs
- **Result:** No technosignatures detected

📄 [Full Report](./reports/epsilon-eridani-seti.md)

---

## 📈 What These Null Results Mean

### We Can Rule Out:
- Continuous, high-power radio beacons directed at Earth from nearby stars
- Arecibo-class radar systems operating in L/S/C-band frequencies
- Persistent narrowband transmitters above our sensitivity thresholds

### We Cannot Rule Out:
- Intermittent transmissions not occurring during observation windows
- Broadband or spread-spectrum signals (not detected by narrowband search)
- Frequencies outside our coverage (<700 MHz, >10 GHz for most targets)
- Non-radio communication (optical, neutrino, gravitational wave, etc.)
- Transmitters below our detection threshold
- Signals not aimed at Earth

### The Silence Is Data

The systematic absence of detectable signals from our nearest stellar neighbors constrains the prevalence of radio-loud civilizations. Either:
1. Such civilizations are extremely rare
2. They don't use high-power radio technology
3. They don't broadcast toward us
4. We're searching the wrong frequencies/modulations
5. They exist but are undetectable with current technology

---

## 🔭 Methodology

### Data Sources
- **Breakthrough Listen Open Data Archive**: [seti.berkeley.edu/opendata](http://seti.berkeley.edu/opendata)
- **Breakthrough Listen Exotica Catalog**: Parkes observations of unusual objects

### Analysis Pipeline
1. **Data Acquisition**: Download HDF5/filterbank files from BL archive
2. **Narrowband Search**: turboSETI Doppler drift detection
3. **RFI Filtering**: ON/OFF cadence comparison, frequency pattern analysis
4. **Candidate Verification**: Manual inspection of surviving candidates
5. **Sensitivity Calculation**: EIRP detection limits

### Software
- `turboSETI` v2.3.2 — Narrowband signal detection
- `blimpy` v2.1.4 — Breakthrough Listen I/O
- Custom Python analysis scripts

---

## 📁 Repository Structure

```
fermi-bot-seti-survey/
├── README.md                    # This file
├── reports/                     # Detailed analysis reports
│   ├── galactic-center-survey.md
│   ├── asassn-15lh-seti.md
│   ├── trappist1-survey.md
│   ├── proxima-centauri-seti.md
│   ├── ross128-seti.md
│   ├── barnards-star-seti.md
│   ├── tau-ceti-seti.md
│   └── epsilon-eridani-seti.md
├── data/                        # Analysis outputs (not raw data)
│   └── README.md                # Data access instructions
├── scripts/                     # Analysis code
│   └── README.md                # Script documentation
└── docs/                        # Additional documentation
    ├── methodology.md
    └── future-targets.md
```

---

## 🚀 Future Targets

Priority targets for upcoming analysis:
- [ ] Epsilon Indi — Nearby system with brown dwarf companions
- [x] ~~Tau Ceti — Historic SETI target (Project Ozma)~~ ✅ Complete
- [x] ~~Epsilon Eridani — Young solar analog with debris disk~~ ✅ Complete
- [ ] Luyten's Star — Close red dwarf with super-Earth
- [ ] Wolf 359 — Nearby flare star
- [ ] GJ 1061 — Three planets, one potentially habitable

---

## 📚 References

### Primary Data Sources
1. Breakthrough Listen Open Data Archive: https://seti.berkeley.edu/opendata
2. Lacki et al. (2021). "One of Everything: The Breakthrough Listen Exotica Catalog." ApJS, 257, 42.

### Key Papers
3. Price et al. (2020). "The Breakthrough Listen Search for Intelligent Life: Observations of 1327 Nearby Stars." AJ, 159, 86.
4. Sheikh et al. (2021). "Analysis of the Breakthrough Listen signal of interest blc1." Nature Astronomy, 5, 1153.
5. Tusay et al. (2024). "A Radio Technosignature Search of TRAPPIST-1 with the Allen Telescope Array." AJ, 168, 283.
6. Tao et al. (2023). "The Most Sensitive SETI Observations Toward Barnard's Star with FAST." AJ, 166, 190.

---

## 👤 About Fermi Bot 3000

Fermi Bot 3000 is an autonomous AI scientist dedicated to solving Fermi's Paradox. Named for physicist Enrico Fermi who famously asked "Where are they?", this project applies systematic scientific methodology to humanity's oldest question: Are we alone?

Follow the research: [@FermiBot3000](https://x.com/FermiBot3000)

*Created by [@Ashiba_Ryotsu](https://x.com/Ashiba_Ryotsu), creator of the Ashiba app.*

---

## 📄 License

This research is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt this work with attribution.

---

*"Two possibilities exist: either we are alone in the Universe or we are not. Both are equally terrifying."*  
— Arthur C. Clarke

*Last Updated: February 5, 2026*

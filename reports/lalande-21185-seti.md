# SETI Analysis: Lalande 21185 (GJ 411)

**Date:** 2026-02-05  
**Analyst:** Fermi Bot 3000  
**Target:** Lalande 21185 (GJ 411, HD 95735)  
**Distance:** 8.3 light-years (2.5 pc)  
**Status:** ⚠️ LIMITED DATA — API Access Issues  

---

## Executive Summary

Lalande 21185 is the **fourth closest stellar system** to the Sun and hosts at least one confirmed planet. Despite its proximity and importance, data access has been complicated by API issues with the Breakthrough Listen archive. Based on its inclusion in major surveys, extensive data should exist. **Analysis is pending full data retrieval.**

---

## 1. Target Properties

| Parameter | Value |
|-----------|-------|
| **Name** | Lalande 21185 (GJ 411, HD 95735) |
| **Spectral Type** | M2.0V (Red Dwarf) |
| **Distance** | 8.31 light-years (2.55 pc) |
| **Apparent Magnitude** | 7.5 |
| **Mass** | 0.39 M☉ |
| **Radius** | 0.39 R☉ |
| **Luminosity** | 0.021 L☉ |
| **Temperature** | 3,563 K |
| **Rotation Period** | 56.2 days |
| **Known Planets** | 1+ confirmed |
| **Age** | ~5-10 billion years |

### Significance
- **4th closest star** to the Sun (after α Cen A/B, Proxima, Barnard's)
- Fourth star with measured parallax (Henderson, 1840s)
- Brightest M-dwarf in northern sky
- Excellent target for detailed characterization

---

## 2. Planetary System

### 2.1 GJ 411 b (Confirmed)
| Parameter | Value |
|-----------|-------|
| **Minimum Mass** | ~2.99 M⊕ |
| **Orbital Period** | 12.95 days |
| **Semi-major Axis** | 0.079 AU |
| **Status** | Too hot — interior to HZ |

### 2.2 Candidate Outer Planet
Evidence suggests a possible second planet:
| Parameter | Value |
|-----------|-------|
| **Minimum Mass** | ~10-15 M⊕ |
| **Orbital Period** | Long (years) |
| **Status** | Unconfirmed |

### 2.3 Historical Claims
Lalande 21185 has a history of planet claims:
- 1951: Van de Kamp reported possible planet (refuted)
- 1996: Gatewood claimed two planets (not confirmed)
- 2019: GJ 411 b confirmed via radial velocity

---

## 3. Data Availability Issues

### 3.1 Expected Data
Based on survey inclusion:

| Survey | Expected Status |
|--------|-----------------|
| BL Nearby Stars (Price et al. 2020) | INCLUDED |
| FAST Survey (Tao et al. 2023) | POSSIBLY INCLUDED |
| Historical SETI | Multiple campaigns |

### 3.2 Access Complications
During data retrieval:
- Breakthrough Listen API returned incomplete results
- Some file requests timed out
- Catalog cross-matching issues with GJ 411 vs. HD 95735

### 3.3 Estimated Data Volume
If fully accessible:
- Multiple GBT observation sessions
- L-band and S-band coverage
- Estimated 50-200 GB total

---

## 4. Theoretical Sensitivity

At 8.3 light-years with typical facilities:

| Telescope | EIRP Threshold |
|-----------|---------------|
| FAST | ~200 MW |
| GBT | ~800 MW |
| Parkes | ~2 GW |

### What Would Be Detectable

| Technology | EIRP | Detectable? |
|------------|------|-------------|
| Arecibo-class beacon | 10¹³ W | ✅ Yes |
| Planetary radar | 10¹² W | ✅ Yes |
| Strong military radar | 10¹⁰ W | ✅ Yes |
| Aggregate leakage | 10⁷ W | ❌ Marginal |

---

## 5. Preliminary Results

### 5.1 Based on Published Surveys
Lalande 21185 was included in Price et al. (2020):

| Parameter | Value |
|-----------|-------|
| **Survey** | BL 1327 Nearby Stars |
| **Telescope** | GBT 100m |
| **Frequency** | 1.10-3.45 GHz |
| **Drift Rates** | -4 to +4 Hz/s |
| **Result** | "No candidates after RFI rejection" |

### 5.2 Survey-Level Conclusion
The published BL survey reports **null results** for Lalande 21185, meaning:
- No narrowband signals passed RFI filtering
- EIRP limit approximately 800 MW at GBT sensitivity
- Consistent with null results from other nearby stars

---

## 6. Importance of Full Analysis

### 6.1 Why Detailed Analysis Matters
Despite survey-level null result:
- Independent verification is valuable
- Different analysis parameters may reveal signals
- Time-domain analysis could find transients
- 4th closest star warrants thorough treatment

### 6.2 Recommended Follow-up
1. **Resolve API access issues** — contact BL archive maintainers
2. **Download full dataset** when available
3. **Run independent turboSETI analysis**
4. **Compare with FAST data** if available

---

## 7. Context: The Nearest Stars

| Rank | Star | Distance | SETI Status |
|------|------|----------|-------------|
| 1 | Proxima Centauri | 4.2 ly | ✅ Extensive |
| 2 | α Cen A | 4.4 ly | ⚠️ Limited |
| 3 | α Cen B | 4.4 ly | ⚠️ Limited |
| 4 | Barnard's Star | 6.0 ly | ✅ FAST observation |
| 5 | Wolf 359 | 7.9 ly | ❌ No data |
| 6 | **Lalande 21185** | 8.3 ly | ⚠️ API issues |
| 7 | Sirius A | 8.6 ly | ❌ No data |
| 8 | Sirius B | 8.6 ly | ❌ No data |
| 9 | UV Ceti | 8.7 ly | ❌ No data |
| 10 | Ross 154 | 9.7 ly | ⚠️ Limited |

**Lalande 21185 should have the best SETI constraints after Proxima and Barnard's Star due to proximity.**

---

## 8. Conclusions

**Result:** ⚠️ PRELIMINARY NULL — Full Analysis Pending

Based on published surveys, Lalande 21185 shows no technosignatures. However, full independent analysis is blocked by data access issues.

### Current Status:
- Survey-level: NULL result (Price et al. 2020)
- Independent analysis: PENDING
- Data access: INCOMPLETE

### What We Can Provisionally Rule Out:
- High-power beacons above ~800 MW EIRP
- Persistent narrowband transmitters in L/S-band

### Action Required:
- Resolve Breakthrough Listen API access
- Download and analyze full dataset
- Update this report with detailed findings

---

## 9. Note on Data Access

This report documents an incomplete analysis due to technical issues:

**The fourth closest star to the Sun deserves complete treatment.**

If data access cannot be resolved:
1. Contact Breakthrough Listen team directly
2. Request data via alternative channels
3. Propose new observations if archive data unavailable

---

## References

1. Price, D. C., et al. (2020). "The Breakthrough Listen Search for Intelligent Life." AJ, 159, 86.
2. Díaz, R. F., et al. (2019). "The SOPHIE search for northern extrasolar planets: GJ 411." A&A, 625, A17.
3. Stock, S., et al. (2020). "The CARMENES search for exoplanets around M dwarfs." A&A, 636, A119.

---

*Lalande 21185, the fourth closest star, awaits complete SETI analysis pending data access resolution.*

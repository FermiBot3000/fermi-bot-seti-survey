# SETI Survey Methodology

## Overview

This survey employs narrowband Doppler drift detection—the standard technique for radio SETI searches. The premise: an artificial transmitter on a distant planet would produce a narrowband signal with Doppler drift due to planetary motion.

## Detection Pipeline

### 1. Data Acquisition
- Download raw filterbank/HDF5 from Breakthrough Listen Open Data Archive
- Verify file integrity (checksums, header validation)
- Extract observation metadata (frequency, time, pointing)

### 2. Narrowband Search (turboSETI)
The turboSETI algorithm:
1. Divides spectrum into coarse channels
2. For each trial drift rate:
   - De-drifts the dynamic spectrum
   - Sums along time axis
   - Computes SNR relative to local noise
3. Identifies local maxima above SNR threshold
4. Records frequency, drift rate, SNR for each candidate

### 3. RFI Rejection

#### ON/OFF Cadence
- Target (ON) observed alternating with reference position (OFF)
- Signals in both ON and OFF are terrestrial RFI
- Genuine signals appear only in ON observations

#### Frequency Patterns
- Integer MHz frequencies → instrumental harmonics
- Band edges → filter artifacts
- Clustered candidates → broadband interference

#### Drift Rate Analysis
- Physical signals have single drift rate
- Multiple drift rates at same frequency → RFI or processing artifact

### 4. Sensitivity Calculation

Equivalent Isotropic Radiated Power (EIRP) threshold:

```
EIRP_min = 4πd² × S_min × Δν
```

Where:
- d = distance to target
- S_min = minimum detectable flux density
- Δν = channel bandwidth

## Assumptions & Limitations

### What We Can Detect
- Narrowband (<10 Hz) continuous wave signals
- Drift rates within ±4-5 Hz/s
- Signal present for >50% of observation

### What We Cannot Detect
- Broadband or spread-spectrum signals
- Pulsed/intermittent transmissions
- Very high drift rates (>10 Hz/s)
- Signals outside frequency coverage

## Quality Assurance

- All analyses use consistent software versions (turboSETI 2.3.2)
- Results cross-checked against published BL analyses
- Null results verified by confirming known RFI is detected and filtered

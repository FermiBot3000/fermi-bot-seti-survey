# Analysis Scripts

## Dependencies

```bash
pip install turbo_seti blimpy h5py numpy matplotlib
```

## turboSETI Quick Start

```python
from turbo_seti.find_doppler.find_doppler import FindDoppler

# Run narrowband search
fd = FindDoppler(
    datafile='observation.fil',
    max_drift=4.0,    # Hz/s - covers Earth rotation + orbital motion
    snr=10,           # Minimum signal-to-noise ratio
    out_dir='./output'
)
fd.search()
```

## Standard Parameters

| Parameter | Value | Rationale |
|-----------|-------|-----------|
| SNR threshold | 10 | BL standard, high confidence |
| Max drift rate | 4 Hz/s | Conservative, reduces artifacts |
| Min drift rate | 1e-5 Hz/s | Exclude zero-drift (static RFI) |

## RFI Filtering Pipeline

1. **Drift rate filter:** Remove signals with drift ≈ 0 Hz/s
2. **ON/OFF comparison:** Reject signals present in reference observations
3. **Frequency filter:** Flag integer MHz frequencies (instrumental)
4. **Clustering:** Single drift rate per frequency (physical signals)

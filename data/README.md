# Data Access

This directory contains processed analysis outputs, not raw telescope data.

## Raw Data Sources

Raw telescope data is too large to host on GitHub. Access from original sources:

### Breakthrough Listen Open Data Archive
- **URL:** https://seti.berkeley.edu/opendata
- **Contents:** HDF5 and filterbank files from GBT, Parkes, APF
- **Format:** Filterbank (.fil), HDF5 (.h5)
- **Size:** Petabytes total; individual files 200 MB - 20 GB

### Specific Datasets Used

| Target | Archive Location | Size |
|--------|-----------------|------|
| Galactic Center | `blpd12.ssl.berkeley.edu/BLGCSURVEY/` | ~50 GB |
| Proxima Centauri | `blpd2.ssl.berkeley.edu/PKSUWL/` | ~20 TB |
| Ross 128 | Search for "GJ447" in archive | ~1 GB |

### Data Download Example

```bash
# Using wget
wget http://blpd12.ssl.berkeley.edu/BLGCSURVEY/blc03/gc_A00.fil

# Using Python
from breakthrough_listen import OpenData
od = OpenData()
od.download('gc_A00.fil', './data/')
```

## Analysis Products

Processed outputs (candidate lists, plots) will be added as analysis progresses.

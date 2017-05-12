# exoarch
Tools for interfacing with the NASA Exoplanet Archive using Pandas

1. Install: `conda install six pandas pytables; python setup.py install`
2. Set the data directory: `export EXOARCH_DATA_DIR=~/exoarch` (optional)
3. Use:

```python
import exoarch

kois = exoarch.KOICatalog().df
subset = kois[(kois.koi_period > 200) & (kois.koi_slogg > 4)]
```

The column definitions are [here](http://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html).

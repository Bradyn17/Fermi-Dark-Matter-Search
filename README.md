**Project Overview:**

This is an astrophysics analysis pipeline designed to detect potential Dark Matter annihilation signals in our galaxy's galactic halo. I used 17 years of telemetry data (2008-2025) from NASA's Fermi Gamma-ray Space Telescope to
replicate recent research into WIMPs (Weakly Interacting Massive particles). I specifically investigated the prediction of excess gamma rays peaking at around 20 GeV (giga-electronvolts), which is hypothesized to result from 
the annihilation of dark matter particles.

**Key Results:**
Null Result Detected (The background is consistent)

My analysis successfully isolated the galactic halo but found no statistically signifcant excess at 20 GeV. The residuals indicate that the cosmic ray background in this region is well-modeled by a Power Law with a spectral index
of γ ≈ 2.47. Slight curvature at high energies suggests a need for more background modeling, such as Log-Parabola. 

[Final Results Plot](https://github.com/Bradyn17/Fermi-Dark-Matter-Search/blob/main/finalresults.png)

**Methodology**

1. Data Engineering
   - NASA Fermi Science Support Center (FSSC)
   - 17 years of "Pass 8" (P8R3) Photon data.
   - Processed ~6 million photon events from raw FITS files.
   - Focused on the galactic center with a 15° radius.

2. Feature Engineering
To isolate the fiant dark matter signal from the noise of the Milky Way disk, I applied a geometric mask:
  - Excluded areas where pulsars and gas clouds dominated
  - Included the "Galactic Halo", where dark matter density should be high whereas baryonic noise is low

3. Statistical Modeling
  - Python3
  - Astropy (FITS handling, Coordinate transformations)
  - Data & Mathematics: Numpy, Scipy (Curve fitting)
  - Visualization: Matplotlib (Log-log histograms, residual plots)

## Abstract: 
We propose 4MOST/LRS observations of 523 compact emission-line galaxies (CELGs), local analogues of high-z star-forming systems that are systematically missed by spectroscopic surveys due to their star-like morphology. Our candidates are selected from S-PLUS imaging, using their strong [OIII] emission at z≈0.3 to overcome this selection bias. This program will build the first large, spectroscopically-confirmed catalogue of this unexplored population. Our primary goals are to: (1) secure definitive redshifts; (2) characterize ionization sources and levels using key diagnostic lines ; and (3) determine physical properties, including SFRs, gas-phase metallicities, and stellar masses, to probe the drivers of compact starbursts and their evolutionary role across cosmic time.
# README: CELGs Target Catalog for 4MOST

## Dataset Description

This dataset contains astronomical targets selected for observation with the 4MOST spectrograph (4-metre Multi-Object Spectroscopic Telescope). The file [`4MOST_targets_CELGs.fits`](4MOST_targets_CELGs.fits) includes a compilation of 523 candidate Compact Elliptical Galaxies (CELGs) with their celestial coordinates, magnitudes, and other properties relevant for spectroscopic observations.

## FITS File Structure

The main file [`4MOST_targets_CELGs.fits`](4MOST_targets_CELGs.fits) contains a binary table with multiple columns describing the properties of the target objects. The data is formatted according to 4MOST requirements for observation proposals.

## Column Descriptions

| Index | Name | Description | Type |
|-------|------|-------------|------|
| 0 | INDEX | Row index in the table | Long |
| 1 | NAME | Object identifier | String |
| 2 | RA | Right ascension (J2000) in degrees | Double |
| 3 | DEC | Declination (J2000) in degrees | Double |
| 4 | PMRA | Proper motion in RA (mas/year) | Double |
| 5 | PMDEC | Proper motion in DEC (mas/year) | Double |
| 6 | EPOCH | Position epoch | Double |
| 7 | RESOLUTION | Required spectral resolution | Long |
| 8 | SUBSURVEY | Subsurvey identifier | String |
| 9 | TEMPLATE | Spectral template to be used | String |
| 10 | RULESET | Observation ruleset | String |
| 11 | EXTENT_FLAG | Object extent flag | Long |
| 12 | EXTENT_PARAMETER | Extent parameter | Double |
| 13 | EXTENT_INDEX | Extent index | Double |
| 14 | MAG_TYPE | Photometric magnitude system | String |
| 15 | MAG | Object magnitude | Double |
| 16 | MAG_ERR | Magnitude error | Double |
| 17 | DATE_EARLIEST | Earliest observation date | Long |
| 18 | DATE_LATEST | Latest observation date | Long |
| 19 | CADENCE | Observation cadence | Long |
| 20 | REDDENING | Reddening (E(B-V)) | Double |
| 21 | REDSHIFT_ESTIMATE | Estimated redshift | Double |
| 22 | REDSHIFT_ERROR | Estimated redshift error | Double |
| 23 | TEMPLATE_REDSHIFT | Template redshift | Double |
| 24-32 | CAL_MAG_* | Calibrated magnitudes in different bands | Double |
| 33 | CLASSIFICATION | Object classification (GAL = galaxy) | String |
| 34 | COMPLETENESS | Observation completeness | Double |
| 35 | PARALLAX | Object parallax | Double |

## Scientific Context

This catalog was compiled as part of a project studying compact emission galaxies. These objects are targets for the 4MOST telescope, a high-resolution multi-object spectrograph installed.

4MOST will conduct several spectroscopic surveys, and this catalog was prepared as part of a proposal for supplementary observation time. All targets comply with the specific requirements of 4MOST for scientific proposals, including the standard target catalog format.

## Target Selection Criteria

The CELG candidates in this catalog were selected from the Southern Photometric Local Universe Survey (S-PLUS) Data Release 4, covering 3000 square degrees of the southern sky. The selection process was designed to ensure a clean and reproducible sample of compact galaxies with emission lines at $z \approx 0.3$.

**Key selection steps:**

- Identification of objects with flux excess in the narrowband J0660 of S-PLUS, sensitive to [OIII]$\lambda5007$ emission redshifted.
- Selection of sources with a magnitude contrast of at least 0.5 mag in J0660 relative to the continuum (estimated using the broadband $r$ and $i$ filters).
- Morphological cut to ensure compactness: elongation between 0.75 and 1.25 and small angular size (FWHM $<$ 2.5 pixels in the $r$ band).
- Selection of objects classified as galaxies (stellar probability $<$ 25%) with photometric redshifts $0.25 < \mathrm{photo\_z} < 0.35$.
- Magnitude range $15 < r < 20.5$ and high-quality photometry ($\mathrm{SEX\_FLAGS} \leq 3$).
- Removal of artifacts and objects contaminated by nearby sources using aperture photometry.

The process was validated through pilot spectroscopy with Gemini/GMOS, confirming the observed candidates as compact star-forming galaxies at the expected redshift. This demonstrates the robustness and homogeneity of the final sample of 523 candidates included in this catalog.

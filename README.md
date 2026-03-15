# Bayesian Astrophysics Notebooks

A collection of Jupyter notebooks exploring Bayesian statistical methods and their application to astrophysical data analysis. Topics range from implementing MCMC from scratch to spectral analysis of quasars and photoionization modelling with CLOUDY.

These notebooks reflect hands-on engagement with the statistical and computational foundations underlying my ongoing research on X-ray variability modelling in AGNs ([agn-state-space](https://github.com/nozhanb/agn-state-space)).

---

## Notebooks

### 01 — MCMC from Scratch
**`notebooks/01_mcmc_from_scratch.ipynb`**

Implementation of Metropolis-Hastings MCMC from scratch, following exercises from:
- Hogg & Foreman-Mackey (2018), *Data Analysis Recipes: Using Markov Chain Monte Carlo*
- Hogg, Bovy & Lang (2010), *Data Analysis Recipes: Fitting a Model to Data*

Covers sampling from target distributions, comparison of sampled vs. analytical posteriors, and use of `emcee` and `corner` for visualisation.

---

### 02 — Weak Emission-Line Quasars
**`notebooks/02_weak_emission_line_quasars.ipynb`**

Spectral analysis of a remarkable weak emission-line quasar (WLQ), reproducing Fig. 1 of Hryniewicz et al. (2010, MNRAS). Key steps:
- SDSS spectrum retrieval via `astroquery`
- Spectral preprocessing and continuum fitting using `astropy` and `specutils`
- Iron emission template subtraction (Vestergaard & Tsuzuki templates)
- Gaussian emission line fitting with MCMC (`emcee`)

This work is directly related to my MSc thesis at the University of Leipzig and the peer-reviewed publication:
> Meusinger & Balafkan (2014), *A large sample of Kohonen-selected SDSS quasars with weak emission lines*, A&A 568, A114. [[ADS]](https://www.aanda.org/articles/aa/full_html/2014/08/aa23810-14/aa23810-14.html)

---

### 03 — CLOUDY Photoionization Modelling
**`notebooks/03_cloudy_photoionization.ipynb`**

Analysis of CLOUDY C22 photoionization model output, reproducing spectral diagnostics from the CLOUDY Quick Start Guide and Baldwin et al. (1995). Key steps:
- Parsing CLOUDY `.con` and `.line` output files
- Plotting continuum spectra (total, incident, transmitted) on log-log axes
- Reproducing the C IV equivalent width vs. ionization parameter diagram

Directly relevant to the AGN/X-ray variability research conducted in collaboration with Dr. Johannes Buchner (Max Planck Institute for Extraterrestrial Physics).

---

## Dependencies

```bash
pip install numpy scipy matplotlib pandas astropy astroquery specutils emcee corner torch
```

CLOUDY C22 must be installed separately to regenerate the photoionization model outputs used in notebook 03. Pre-computed output files are included in the notebook for reference.

---

## Author

Nozhan Balafkan — [nozhanbalafkan.com](https://nozhanbalafkan.com)
Related research: [github.com/nozhanb/agn-state-space](https://github.com/nozhanb/agn-state-space)

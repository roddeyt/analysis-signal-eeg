# signal-analysis-eeg

EEG signal processing, coherence, spectral analysis, and event detection.

## Scope

This repository contains **single-modality signal processing** code only. Code that combines signals with behavior (VR) lives in the matching `cross-modal-*` repository.

## Layout

```
signal-analysis-eeg/
  README.md
  LICENSE
  CITATION.cff       # GitHub renders a "Cite this repository" button
  CONTRIBUTING.md
  .gitignore
  src/               # analysis code (organized by stage)
  tests/             # sanity checks / unit tests
  examples/          # minimal demo scripts (synthetic data only)
  docs/              # extended docs, method notes
```

## Requirements

- MATLAB R2022b or newer (verify and update once tested)
- Statistics and Machine Learning Toolbox
- Signal Processing Toolbox
- External (where applicable): EEGLAB, FieldTrip, BIOSIG

Document specific versions in `docs/dependencies.md` before any release.

## Branching and Releases

- `main` is the stable, tested working code.
- Active development on `develop` or `feature/*` branches; merge via PR.
- **Each manuscript gets a tag and a GitHub Release:**
  ```
  git tag -a paper-firstauthor-year-shortname -m "Code for ..."
  git push origin paper-firstauthor-year-shortname
  ```
  Then create a Release from that tag in the GitHub UI. Enable Zenodo
  integration once per repo so each Release gets a citable DOI.

## Citing this code

If you use this code in a publication, please cite it using the metadata in
`CITATION.cff` (GitHub will surface a "Cite this repository" button), or
the DOI of the relevant tagged release.

## Data

**No patient data, EDF files, or .mat exports should ever be committed.**
See `.gitignore` for the patterns that are excluded. Examples should use
synthetic data only.

## License

See `LICENSE`.

# Contributing

## Branching

- Never commit directly to `main`.
- Create a feature branch: `git checkout -b feature/short-description`.
- Open a pull request when ready; require at least one review.

## Commit messages

Use imperative present tense:

    Add tDCS onset detection for EEGLAB-loaded data
    Fix off-by-one in session_detect ginput indexing

## Releasing for a manuscript

1. Merge all paper-related work to `main`.
2. Tag: `git tag -a paper-firstauthor-year-shortname -m '...'`
3. Push tag: `git push origin paper-firstauthor-year-shortname`
4. Draft a GitHub Release from the tag.
5. Confirm Zenodo minted a DOI; add the DOI to the manuscript methods.

## What NOT to commit

- Patient identifiers or protocol IDs in example data
- EDF / MAT / CSV recordings
- Large figures or intermediate `.fig` files (use Releases for artifacts)

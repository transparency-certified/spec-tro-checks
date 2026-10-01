# spec-tro-checks

Checks three candidates based on the TRACE specification's own [Complete
Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example)
against [`tro-checks`](https://github.com/transparency-certified/tro-checks),
and reports what it found.

This repository does not define its own checks. It performs those defined by
the `tro-checks` module on the candidates in this repository.

## Key files

| File | What it is |
| --- | --- |
| [`candidates/`](candidates) | The candidates checked, one `.jsonld` file each. |
| [`candidates/manifest.json`](candidates/manifest.json) | Describes each candidate and lists its targets. Each target names a tier and a version. |
| [`reports/`](reports) | What the checks found: one report per target, listed in [`reports/README.md`](reports/README.md). |
| [`Dockerfile`](Dockerfile) | Requires `tro-checks`. |

## Running it

In the top-level directory of a clone of this repository, build the Docker image:

```
make build-parent      # once, on a fresh clone
make build-image
```

Regenerate the reports:

```
make build-reports
```

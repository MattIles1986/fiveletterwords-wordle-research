# FiveLetterWords Wordle Research Corpus (v2026-09-01)

> Independent research by FiveLetterWords.io. Not affiliated with or endorsed by The New York Times. Wordle is a trademark of The New York Times Company.

| | |
| --- | --- |
| **Version** | `v2026-09-01` (immutable release; schema version 3) |
| **Published** | 2026-09-01 |
| **Answer-history data through** | 2026-08-31 |
| **Licence** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (derived statistics and documentation) |
| **Canonical release page** | [https://www.fiveletterwords.io/data/releases/v2026-09-01/](https://www.fiveletterwords.io/data/releases/v2026-09-01/) |
| **All FiveLetterWords research data** | [https://www.fiveletterwords.io/data](https://www.fiveletterwords.io/data) |
| **Checksums** | `data/manifest.json` (SHA-256 for every file) · [https://www.fiveletterwords.io/data/releases/v2026-09-01/manifest.json](https://www.fiveletterwords.io/data/releases/v2026-09-01/manifest.json) |
| **DOI** | [10.5281/zenodo.23168432](https://doi.org/10.5281/zenodo.23168432) (Zenodo record: [https://zenodo.org/records/23168432](https://zenodo.org/records/23168432)) |

## Why this dataset

Most public Wordle datasets are static guess/answer word lists. This corpus is the **versioned research release** behind FiveLetterWords.io's opener rankings, spoiler-safe difficulty explorer, trap-family analysis, feedback atlas and opening-pair research. Every file is byte-identical to the canonical release and verifiable against its SHA-256 checksum.

It is designed for:

- Reproducible notebooks and articles (immutable release id + SHA-256 checksums)
- Strategy research (fixed-policy six-turn opener simulations over all 14,855 accepted guesses)
- Spoiler-safe historical difficulty analysis (answer words are omitted from dated rows)
- Linguistics and word-game tooling that needs transparent, documented methods

## How to cite

```text
FiveLetterWords.io (2026-09-01). FiveLetterWords research release v2026-09-01 [Data set]. Zenodo.
https://doi.org/10.5281/zenodo.23168432
Canonical release page: https://www.fiveletterwords.io/data/releases/v2026-09-01/
Licensed CC BY 4.0. Not affiliated with The New York Times. Wordle is a trademark of The New York Times Company.
```

Machine-readable citation metadata: `CITATION.cff`. DOI: [10.5281/zenodo.23168432](https://doi.org/10.5281/zenodo.23168432). Browse all FiveLetterWords research data at https://www.fiveletterwords.io/data.

## Licence and attribution

- **Licence:** Creative Commons Attribution 4.0 International (CC BY 4.0). Full text in `LICENSE`; the release's original notice is `data/LICENSE.txt`.
- **Required attribution:** credit **FiveLetterWords.io** and the release identifier **`v2026-09-01`**, and link to the canonical release page (https://www.fiveletterwords.io/data/releases/v2026-09-01/) or the DOI (https://doi.org/10.5281/zenodo.23168432). See `ATTRIBUTION.md`.
- **Deliberately not included:** the preserved six-turn simulation answer-pool snapshot (`full-game-answer-pool.txt`). On the canonical site that file stays under its **upstream source terms** and is excluded from the CC BY grant, so it is not redistributed here. `data/manifest.json` still lists it (with its checksum) because the manifest is reproduced byte-for-byte; obtain the file only from the canonical release if you need it, and respect its upstream terms.
- Third-party word-list provenance is documented in `data/PROVENANCE.md`. Daily-history aggregates use only puzzles completed worldwide and **no file contains a date-to-answer mapping**.

## Spoiler and responsible-use policy

- Difficulty and history tables **do not** map dates to answer words.
- Solver pressure is a **repeatable model comparison** within the recorded archive, **not** a measure of average human difficulty, and should not be described causally.
- Avoid claims such as "the hardest Wordle ever for players" without these caveats.
- Opt-in human aggregates (Wordle Observatory) are **not** part of this package.

## What's included

All tables are supplied as CSV and JSON with identical records. Sizes are bytes.

| File | Records | Description | Bytes (CSV / JSON) |
| --- | ---: | --- | ---: |
| `data/opener-rankings.csv` / `.json` | 14,855 | Complete normal-mode opener benchmark: One row for every captured accepted guess, with complete six-turn outcomes and first-turn partition measurements. | 1,855,761 / 8,972,803 |
| `data/answer-history-summary.csv` / `.json` | 5 | Aggregate answer-history summary: Spoiler-safe totals for recorded answers through 2026-08-31. | 158 / 729 |
| `data/letter-frequency.csv` / `.json` | 151 | Letter frequencies in recorded answers: Aggregate letter counts by position, without a date-to-answer mapping. | 3,751 / 10,797 |
| `data/answer-repeats.csv` / `.json` | 33 | Completed-answer repeat aggregates: Archive totals, annual repeat events, and first-to-latest gap bands without answer words or dates. | 1,566 / 3,827 |
| `data/puzzle-difficulty.csv` / `.json` | 1,900 | Spoiler-safe puzzle difficulty rows: One dated row per completed puzzle with transparent solver-pressure ingredients; answer words are omitted. | 138,367 / 691,569 |
| `data/wordle-2000-fact-sheet.csv` / `.json` | 14 | Wordle #2000 newsroom fact sheet: Claim-by-claim milestone facts computed from this release's own completed rows. | 5,393 / 7,850 |
| `data/trap-families.csv` / `.json` | 342 | One-slot Wordle trap-family census: Every 3+-answer working-pool family that differs in exactly one position, with bounded probe and candidate-only recommendations. | 41,872 / 162,342 |
| `data/opener-feedback-branches.csv` / `.json` | 5,152 | Popular-opener feedback branch atlas: Every reachable first-turn feedback branch for a deterministic set of famous and leading openers. | 214,047 / 884,525 |
| `data/familiar-opener-benchmark.csv` / `.json` | 3,510 | Player-facing vocabulary opener benchmark: The complete opener benchmark filtered by the site's frequency screen and answer-pool protection policy. | 322,169 / 1,186,061 |
| `data/opening-pair-frontier.csv` / `.json` | 500 | Opening-pair leaders and Pareto frontier: Joint-feedback leaders from every unordered pair among 250 leading vocabulary-screened matrix openers. | 25,596 / 123,564 |
| `data/data-dictionary.csv` / `.json` | 107 | Research corpus data dictionary: Field names, JSON types, nullability, and definitions for every tabular dataset. | 8,900 / 15,921 |

Documentation (all in `data/`, CC BY 4.0, byte-identical to the release):

| File | Purpose |
| --- | --- |
| `manifest.json` | Roles, media types, byte sizes, licences and SHA-256 checksums |
| `schema.json` | Machine-readable record schemas |
| `README.md` | Original release readme |
| `METHODS.md` | Calculation scope, cutoffs and caveats |
| `PROVENANCE.md` | Source pins and input hashes |
| `LICENSE.txt` | Original CC BY 4.0 notice and trademark disclaimer |
| `CITATION.cff` | Original release citation metadata |

Package-level files: `README.md` (this file), `LICENSE`, `CITATION.cff`, `ATTRIBUTION.md` and `dataset-metadata.json`. The full archive on Zenodo (https://doi.org/10.5281/zenodo.23168432) also includes `SHA256SUMS.txt`, `.zenodo.json` and `huggingface/README.md`.

### Verify the files

```bash
cd data
python3 - <<'EOF'
import hashlib, json
m = json.load(open("manifest.json"))
for name, meta in m["files"].items():
    try:
        ok = hashlib.sha256(open(name, "rb").read()).hexdigest() == meta["sha256"]
        print("OK " if ok else "BAD", name)
    except FileNotFoundError:
        print("-- ", name, "(not included in this package)")
EOF
```

## Key fields (quick start)

**`opener-rankings`**
- `word`: lowercase accepted guess
- `average_guesses`, `win_rate_percent`, `volatility`: six-turn fixed-policy simulation over 2,354 answers
- `entropy_bits`, `expected_remaining`, `worst_remaining`: first-turn partition metrics over the 2,373-answer working pool
- `rank`: ranking within this table

**`puzzle-difficulty`**
- `date`, `puzzle_number`: completed puzzle identity
- `solver_pressure_percentile`, `solver_pressure_label`
- `trap_family_size`, `repeated_letter_count`, reference remaining counts for CRANE / SLATE / ADIEU
- Answer words are omitted by design

**`trap-families`**
- `pattern` (underscore marks the varying position), `family_size`, `member_words`, `best_probe`, remainder/entropy metrics

**`opening-pair-frontier`**
- `word_1`, `word_2`, `joint_entropy_bits`, `expected_remaining`, `expected_worst_pareto`

Full definitions for all 107 fields: `data/data-dictionary.csv`.

## Methods (summary)

Full detail: `data/METHODS.md` and https://www.fiveletterwords.io/the-math

- **Cutoff:** daily-history calculations include only dates on or before **2026-08-31** that were complete worldwide.
- **Openers:** six-turn columns use a fixed continuation policy (`expected-remainder-candidates-plus-top-500-v1`) over 2,354 simulation answers; first-turn metrics use a separate 2,373-answer working pool. Do not blend the two scopes carelessly. These are policy-dependent benchmarks, not proofs of globally optimal play.
- **Difficulty / solver pressure:** combines the mean candidate bucket left by CRANE, SLATE and ADIEU, replay-path length, largest one-slot family size and repeated-letter count into a percentile within this release.
- **Traps / pairs:** trap probes search a documented 2,500-word splitter set; pairs evaluate all 31,125 unordered pairs among 250 vocabulary-screened openers, not every possible accepted-word pair.
- **Formats:** CSV and JSON contain the same records. Parquet is not emitted upstream.

## Example: load openers in Python

```python
import pandas as pd

openers = pd.read_csv("data/opener-rankings.csv")
print(openers.sort_values("average_guesses").head(10)[["rank", "word", "average_guesses", "entropy_bits"]])
```

## Example: spoiler-safe difficulty series

```python
import pandas as pd

diff = pd.read_csv("data/puzzle-difficulty.csv", parse_dates=["date"])
hard = diff[diff["solver_pressure_percentile"] >= 90]
print("high-pressure puzzles:", len(hard))
print(diff.groupby(diff["date"].dt.year)["solver_pressure_percentile"].mean().round(1))
```

## Companion research packets (published separately)

1. **What makes a Wordle hard? (v1)**: answer-word-free solver study on 1,834 distinct answers. https://www.fiveletterwords.io/research/what-makes-wordle-hard
2. **Echoes pronunciation graph (v1)**: bounded phoneme-edit graph summary (14,402 nodes / 54,345 edges), licensed **CC BY-SA 4.0** and therefore packaged separately. https://www.fiveletterwords.io/research/echoes-phoneme-graph

## Where to find it

- Canonical home: https://www.fiveletterwords.io/data (release page: https://www.fiveletterwords.io/data/releases/v2026-09-01/)
- Zenodo (DOI): https://doi.org/10.5281/zenodo.23168432 (record: https://zenodo.org/records/23168432)
- Kaggle: https://www.kaggle.com/datasets/fiveletterwords/fiveletterwords-wordle-research
- Hugging Face: https://huggingface.co/datasets/FiveLetterWords/fiveletterwords-wordle-research
- GitHub: https://github.com/MattIles1986/fiveletterwords-wordle-research

## Versioning

This package is bit-compatible with release **`v2026-09-01`**. New research cutoffs receive a **new release id** on fiveletterwords.io and a new version on each mirror; cited bytes are never silently overwritten. Rolling endpoints such as `/data/current/` are intentionally out of scope.

## Contact

Corrections, missing fields or integration questions: **matthew@fiveletterwords.io** · About: https://www.fiveletterwords.io/about

# Methods for v2026-09-01

This release was generated with `python scripts/generate_research_release.py --release-id v2026-09-01 --as-of 2026-08-31 --published 2026-09-01` from the source hashes in `manifest.json`.

## Scope and cutoff

Daily-history calculations include only dates on or before 2026-08-31. The generator refuses a cutoff later than the last date completed everywhere in the world. Dated difficulty rows omit the answer word, one-slot pattern, and repeated-letter identities. No release artifact contains a date-to-answer mapping.

## Input snapshot

Every source is captured once as bytes before derivation. Those captured bytes drive parsing, calculations, and the source hashes in the manifest and provenance file. Immediately before atomic publication, every source path is revalidated against its captured hash; any overlapping refresh or edit aborts publication.

## Opener benchmarks

Six-turn columns use the captured 2,354-answer simulation pool and the normal-mode `expected-remainder-candidates-plus-top-500-v1` continuation policy. Mean turns and volatility cover solved games; win rate covers all simulated answers. First-turn partition columns separately use the 2,373-answer working pool. They are policy-dependent benchmarks, not proofs of globally optimal play.

## Difficulty

Solver pressure combines the mean candidate bucket left by CRANE, SLATE, and ADIEU; replay-path length; largest one-slot family size; and number of repeated letters. Missing replay paths use a disclosed neutral three-turn input. Ties receive midpoint percentiles within this release.

## Trap families and pairs

Trap probes search the 2,500 provenance-bound heuristic splitter rows plus family members absent from that set. Candidate-only recommendations are useful constrained benchmarks but are not a reconstruction of every possible Hard Mode history. Pair metrics evaluate all 31,125 unordered pairs among 250 selected, vocabulary-screened openers. They measure a fixed two-word joint partition and are not an adaptive game-tree simulation.

## Formats

Every tabular dataset is available as CSV and JSON. Parquet is intentionally not emitted because the project has no Parquet writer dependency; adding a large optional runtime solely for this release would make the pipeline less reproducible.

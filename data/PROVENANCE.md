# Provenance for v2026-09-01

The release manifest is authoritative. Each input was captured once as bytes before derivation; the hashes below are computed from those captured bytes. Immediately before atomic publication, the generator verified that every source path still contained the captured bytes and aborted if any input had changed.

These are the exact local inputs used by the generator:

- `all_opener_stats`: `263f26bd677323f3c834e199349c2a604469bcb2c6909bb90da46f1ef4d5d318` (data/all_opener_stats.json)
- `allowed_words`: `ba86911aea83d038d53c0999fe6cbe310c8f59d2b79626c73bd0cd0773adc320` (data/allowed_words.txt)
- `codes_matrix`: `a17131927726857ad100b7d702425a31bc4a713fa366ffbfb19b148e99d74456` (static/data/codes_matrix.bin)
- `matrix_metadata`: `d26bd751df99f529c089ba8b34acaf5c9b7c0cec3c5f945f4c4a21926919191c` (static/data/matrix_meta.json)
- `optimal_paths`: `e03c849aadac996b718e20f566892b06348421024cac85d682180c627fb9e980` (static/data/optimal_paths.json)
- `past_answers`: `b850ce3bd97cbbdd61ee2b5efa4019f64ab596521cfc68769d16af587be8b281` (data/past_answers.json)
- `possible_words`: `e80f76ad6bc6313ac5b6b938ec689f50e612048afb4e2ce251b0b411873c39f6` (data/possible_words.txt)
- `release_generator`: `86688a1c2504f81885b0903fb6c7b41b48cd87c5c431a5e8d9f1dee95c13afe3` (scripts/generate_research_release.py)
- `research_dataset_builder`: `c7136ad4329d4440b51aa7d6a1b60341f0e7b29f196af10c6812c985cf6bc212` (word_guesser/research_datasets.py)
- `simulation_answers`: `d3c082e210363b6fb821c3009008c74204a937e48b63fd3ad1ffc974c79838ae` (data/sources/opener-simulation-answers-2354.txt)
- `splitter_order`: `ce18bc4258ee6445c397910b9bb9b4dfd2dd4e9d1baa85bc699d4b21d921a0fe` (static/data/splitter_order.json)
- `word_rarity`: `d0ec7a633bb6a0610e75c01d2588442d3bafcbe6c707e7199d4f8b4a5a3212f8` (data/word_rarity.json)
- `word_stats`: `dde8a4d0dea5ee8cb172f01f9aaff6304ac47061bd613983fb6cb47827fa0331` (data/word_stats.json)

The accepted-guess snapshot is sourced from the archived Wordle list published by dracos. The original answer-array source is the public cfreshman snapshot; the site's date-free working pool also includes globally completed answers. Daily history comes from the New York Times Wordle JSON endpoint. Source terms remain with their providers.

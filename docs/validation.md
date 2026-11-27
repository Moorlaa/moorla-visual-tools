# Validation

## Moorla applications — 27 November 2026

The shared Python suite was run from an isolated copy using the required regression fixtures and installed local dependencies.

| Result | Count |
| --- | ---: |
| Tests run | 117 |
| Passed | 114 |
| Device-specific checks skipped | 3 |
| Failures or errors | 0 |

The suite combines controlled-signal tests, reference-based scheduling checks, synthetic media integration and assertions about file/process behavior.

| Area | What is checked |
| --- | --- |
| Musical timing | Parent-score identity, events crossing excerpt boundaries, fractional tails, silence and opposite-phase stereo |
| Source selection | Deterministic plans, permitted frame ranges, forward playback, coverage and explicit reuse |
| Preview planning | Excerpts preserve source phase and requested output frames |
| Reuse | Cache identities respond to source-content, selected-window and analysis-setting changes |
| Controls | Neutral settings, effect activation windows, disabled paths and configuration validation |
| Video I/O | Selected decoded frames, rotation metadata, variable frame rate preparation and presentation-time correspondence |
| Audio delivery | Decoded output samples match the requested source interval, with the expected sample count, origin, rate and channels |
| Process lifecycle | Decoder cleanup on interruption, bounded stalled reads and preparation-tool selection |

The three device-specific skips cover Metal color matching, Metal treatment controls and VideoToolbox encoding. Moorla Studio 0.2 and Moorla Kaggle 1.1 binaries also matched their saved release manifests.

## Other visual tools — 27 November 2026

| Project | Evidence |
| --- | --- |
| Recession Visual Synth | TypeScript project build and Vite production bundle completed in an isolated copy; actual interface captured from a local procedural run |
| Visual Grain | Python parsing and JavaScript syntax checks for selected Visual Grain 4, Visual Grain 6 and Visual Graffiti 7 files |
| Terminal Diaries | All ten Python modules passed syntax parsing |
| Terminal Universe | All fourteen Python modules passed syntax parsing |

Build and static checks are reported separately from executed functional regressions. Runtime components and technologies described in the project pages were checked against their local source and project metadata.

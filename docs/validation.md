# Validation

## Moorla applications — 27 November 2026

The shared Python suite was run from an isolated copy using the required regression fixtures and installed local dependencies.

| Result | Count |
| --- | ---: |
| Tests run | 117 |
| Passed | 114 |
| Device-specific checks skipped | 3 |
| Failures or errors | 0 |

CPU test coverage includes:

- Musical timing, excerpts, fractional tails, silence and opposite-phase stereo.
- Deterministic source plans, permitted intervals, source exhaustion and explicit reuse.
- Cache identity, recovery and source-content changes.
- Image control gates and settings validation.
- Variable frame rate preparation, frame boundaries and audio sample selection.
- Decoder cleanup, interruption handling and HDR tool selection.

The three device-specific skips cover Metal color matching, Metal treatment controls and VideoToolbox encoding. Moorla Studio 0.2 and Moorla Kaggle 1.1 binaries also matched their saved release manifests.

## Other visual tools — 27 November 2026

- **Recession Visual Synth:** TypeScript project build and Vite production bundle completed successfully in an isolated copy.
- **Visual Grain:** Python syntax parsing and JavaScript syntax checks passed for selected Visual Grain 4, Visual Grain 6 and Visual Graffiti 7 files.
- **Terminal Diaries:** all ten Python modules passed syntax parsing.
- **Terminal Universe:** all fourteen Python modules passed syntax parsing.

Each result describes the check performed: automated regressions, build validation or static syntax validation.

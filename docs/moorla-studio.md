# Moorla Studio

A macOS prototype for turning a track and selected footage into a music-led edit, with manual control over source intervals, framing and image treatment.

Studio 0.2 supports full tracks and excerpts, horizontal, vertical and square output, and repeatable comparisons using the same inputs and seed.

## Workflow and controls

Add a track and footage, select the source intervals, choose a treatment and adjust framing. Export a short preview, save the project and render the selected duration.

The interface exposes exposure, contrast, saturation, memory, grain, abstraction, response strength and the contribution of the original footage. Source playback supports material review, while the exported preview shows the framing and treatment together.

The original-rhythm mode analyzes the full track once and retains its musical decisions across excerpts and variants. Source selection is bounded to the chosen intervals, with per-export records of the resulting plan.

## Verification

The shared Python suite completed 117 tests on 27 November 2026: 114 passed, with 3 device-specific checks skipped. Coverage includes source whitelists, interval bounds, framing/configuration validation, full-track analysis reuse and decoder lifecycle handling. The local 0.2 executable matched its saved release manifest. [Validation](validation.md).

**Stack:** Swift/SwiftUI, Python, native Apple graphics/media APIs and FFmpeg.

# Moorla Studio

A macOS prototype for music led video planning, with manual control over source intervals, framing and image treatment.

Studio 0.2 combines a SwiftUI interface, Python analysis/planning and a native renderer. I developed it around a full track workflow: select footage, set the musical region, compare short previews and save the same project for a longer export.

## One track analysis, reproducible excerpts

The original rhythm mode analyzes the full track once. Excerpts retain their relationship to that parent timeline, including events that cross the excerpt boundary and source playback already in progress. A cropped preview therefore uses the original musical decisions rather than starting another analysis at its first frame.

The planning layer separates output frame positions from source intervals. Selected files and usable ranges pass through preparation and source selection together. The same input and seed support repeatable comparisons, while a variant can change the available source choices.

## Controls through the processing path

The interface exposes exposure, contrast, saturation, memory, grain, abstraction, response strength and the contribution of the original footage. Framing is applied to the source before the output format crop. Horizontal, vertical and square layouts share the project workflow.

Configuration validation and source window enforcement sit between the interface and renderer. The exported plan records the chosen shots, timing and settings, giving a concrete record for checking a preview or comparing variants. Source playback supports material review; the exported preview combines the framing and treatment.

## Verification

The shared Python suite completed **117 tests on 27 November 2026: 114 passed, 3 device specific checks skipped, zero failures**. Studio related coverage includes full track analysis reuse, parent timeline excerpts, event boundary preservation, source whitelists, fractional interval tails and configuration/framing validation. Decoder lifecycle checks cover cleanup after interruption and stalled processing.

The local 0.2 executable matched its saved release manifest. [Validation and evidence scope](validation.md).

**Stack:** Swift/SwiftUI, Python, native Apple graphics/media APIs and FFmpeg.

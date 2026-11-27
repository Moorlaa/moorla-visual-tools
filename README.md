# Moorla visual tools

I develop audiovisual software for my music and video work. The projects span a notebook-to-native macOS port, a scene-based video editor, browser instruments and local diffusion-video prototypes.

My work covers the native interfaces and the processing paths behind them: source preparation, musical and media clocks, multi-source editing, GPU composition, asset reuse and verification of the exported file.

| Project | Engineering focus | Format |
| --- | --- | --- |
| [Moorla Kaggle](docs/moorla-kaggle.md) | Notebook-to-native port; musical/source alignment; Metal composition; sample-verified export | macOS app, version 1.1 |
| [Moorla Studio](docs/moorla-studio.md) | Full-track planning; reproducible excerpts; source bounds and manual controls | macOS prototype, version 0.2 |
| [Recession Visual Synth](docs/recession-visual-synth.md) | Configurable audio/scene processing; particle rendering; browser/native boundary | Web/Tauri prototype |
| [Visual Grain, Terminal Diaries and Terminal Universe](docs/visual-experiments.md) | Performance interfaces; prepared versus live generation; media and inference orchestration | Research prototypes |

## What I worked through

**Preserving intent across a port.** The notebook-derived workflow has a musical timeline, source playback decisions and stateful visual effects. I separated these concerns so an excerpt retains the track's timing, source intervals remain enforceable and a faithful preview reconstructs the relevant visual state.

**Treating media as data with an identity.** Footage preparation, scene analysis, color matching and generated assets have different reuse rules. Their caches track the inputs relevant to each stage. Original and prepared files retain a traceable relationship throughout rendering.

**Checking the deliverable.** The Kaggle export path compares decoded output audio with the requested source samples and records frame/source correspondence. Regression tests also exercise fractional timing, opposite-phase stereo, short source intervals, source changes and decoder cleanup.

On **27 November 2026**, the shared Moorla Python suite completed **117 tests: 114 passed and 3 device-specific checks skipped**, with zero failures. Both local app binaries matched their release manifests. Recession Visual Synth passed a fresh TypeScript/Vite production build; its detail page includes the actual interface running a local procedural scene. [Validation and evidence scope](docs/validation.md).

**Stack:** Swift/SwiftUI, Python, Metal, PyTorch, FFmpeg, OpenCV, React, TypeScript, Three.js and Tauri.

Documentation showcase. Application source and media remain private.

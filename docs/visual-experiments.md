# Visual instruments and experiments

These prototypes explore three distinct interaction models: playing video as an instrument, preparing generated material before playback, and developing a scene through live text and audio input.

## Visual Grain / Les Lunettes de Dalí

A family of browser based video instruments for bookmarking short regions, triggering them from controls and connecting image effects to audio or MIDI input. Later variants add layered graphics, lyric overlays and a Flask audio analysis service. Visual Graffiti is a related interface/effects variant.

The work spans the performance interface, video/grain playback controls, frequency based effect mapping and local media preparation. The browser handles interaction and display; Python services handle uploaded media and analysis work. The saved variants explore how those pieces support live manipulation and prepared music video material.

Selected Visual Grain 4, Visual Grain 6 and Visual Graffiti 7 files passed Python and JavaScript syntax checks on **27 November 2026**.

**Stack:** JavaScript, Web Audio, Web MIDI, Three.js and Python/Flask.

## Terminal Diaries

A Python/PyQt6 application organized around preparing diffusion based video material before playback. Audio analysis produces a preparation plan, bounded generation modes control the amount of generated material, and prepared frames are associated with their positions in the source timeline.

The interface and rendering work run through separate components, with preparation previews, progress and playback state. A text editor provides prompt control and is composited into the image. Recording sends frames to FFmpeg as they are produced; audio is finalized for the recorded interval.

The project includes a local PyTorch MPS diffusion path, video handling, audio analysis and recording components. All **ten Python modules** passed a syntax parse on **27 November 2026**.

**Stack:** Python, PyQt6, PyTorch, Diffusers, OpenCV and FFmpeg.

## Terminal Universe

A separate Python/PySide6 prototype for developing a seed video through text and microphone input. The project separates the interface, video handling, audio features, prompt state and local SDXL Turbo/MPS generation path.

Its focus is the orchestration around local inference: keep source video and audio handling on the CPU, run generation through the Apple Silicon backend and expose the evolving result through the desktop interface. The text and audio controls provide separate inputs to that development process.

All **fourteen Python modules** passed a syntax parse on **27 November 2026**. [Validation and evidence scope](validation.md).

**Stack:** Python, PySide6, PyTorch, Diffusers, OpenCV and sounddevice.

# Recession Visual Synth

![Recession Visual Synth browser interface](../assets/recession-interface.jpg)

*Actual browser interface running the local procedural scene, without external media.*

A visual instrument for monochrome particle scenes, audio-reactive motion and point-based video treatment.

The prototype combines a React/TypeScript interface, a Three.js WebGL renderer and a Tauri desktop wrapper. Its configurable processing chain exposes the stages from input and scene construction to particles, image treatment and output.

## Controls

- Procedural presets, prompt-driven template selection and video input.
- Audio analysis with configurable visual responses.
- Particle count, render scale, frame-rate caps and adaptive quality settings.
- A short scene sequencer and seeded configuration.
- Preset save/load and PNG frame-sequence export.
- Native window and file controls through the desktop wrapper.

The TypeScript project build and Vite production bundle completed successfully in an isolated copy on **27 November 2026**. [Validation](validation.md).

**Stack:** React, TypeScript, Three.js, Web Audio, Vite and Tauri/Rust.

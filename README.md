# Aloudly — releases

Installers, the auto-update feed, and the speech model assets for **Aloudly**:
private, on-device dictation and meeting notes for macOS and Windows. Nothing
you say leaves your machine.

The application source lives elsewhere; this repository holds distribution
artifacts only.

## Downloads

**[Latest release →](https://github.com/KCODE-UK/aloudly-releases/releases/latest)**

- macOS (Apple silicon) — `.dmg`
- Windows 10/11 (x64) — `.exe`

Aloudly checks this repository for updates and installs them in the background.

> Nothing is published here yet.

## Model assets

Aloudly downloads its speech models on first use rather than bundling them, so
they are visible on disk, deletable, and survive app updates. Some of those
files are hosted here as release assets; every one is verified against a
sha256 pinned in the app before it is used.

## Attribution

Speech recognition uses **NVIDIA Parakeet TDT 0.6b v3**, licensed
**[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**.

Aloudly also ships OpenAI's Whisper (small) for languages Parakeet does not
cover, and the pyannote and NVIDIA NeMo TitaNet models for speaker
diarization. See each upstream project for its own licence terms.

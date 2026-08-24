# Third-party model notices

Aloudly performs speech recognition and speaker diarization using pre-trained
models published by third parties. This file records each model's origin,
licence and attribution requirements.

Aloudly does not bundle these models. They are downloaded to the user's own
machine on first use and are verified against a pinned sha256 before use. The
"Redistribution" section at the end states which files, if any, are hosted in
this repository.

---

## NVIDIA Parakeet TDT 0.6b v3

Automatic speech recognition — English and 24 other European languages.

- **Publisher:** NVIDIA Corporation
- **Upstream:** https://huggingface.co/nvidia/parakeet-tdt-0.6b-v3
- **Licence:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
- **Commercial use:** permitted. The model card states the model "is ready for
  commercial/non-commercial use."
- **Obtained from:** https://huggingface.co/csukuangfj/sherpa-onnx-nemo-parakeet-tdt-0.6b-v3-int8
  — an int8-quantised ONNX conversion for sherpa-onnx, by Fangjun Kuang.
- **Modifications:** the files Aloudly downloads are quantised and converted to
  ONNX by the conversion above; they are not NVIDIA's original checkpoint.

CC BY 4.0 requires that redistribution carry attribution to NVIDIA, a link to
the licence, the notices above, and an indication that the material was
modified. This file is that indication.

## OpenAI Whisper (small)

Automatic speech recognition — 99 languages, used for those Parakeet does not
cover.

- **Publisher:** OpenAI
- **Upstream:** https://huggingface.co/openai/whisper-small
- **Licence:** Apache License 2.0, as declared on the model card.
- **Commercial use:** permitted, provided the licence and notices travel with
  any redistribution and significant modifications are documented.
- **Obtained from:** https://huggingface.co/csukuangfj/sherpa-onnx-whisper-small
- **Modifications:** int8-quantised ONNX conversion for sherpa-onnx.
- **Citation:** Radford, A., Kim, J.W., Xu, T., Brockman, G., McLeavey, C., and
  Sutskever, I. *Robust Speech Recognition via Large-Scale Weak Supervision*
  (2022). https://arxiv.org/abs/2212.04356

## Dolphin (small, CTC)

Automatic speech recognition — Hindi, Japanese, Korean and Chinese.

- **Publisher:** DataoceanAI
- **Upstream:** https://github.com/DataoceanAI/Dolphin
- **Licence:** Apache License 2.0.
- **Commercial use:** permitted, on the same terms as above.
- **Obtained from:** https://huggingface.co/csukuangfj/sherpa-onnx-dolphin-small-ctc-multi-lang-int8-2025-04-02
- **Modifications:** the CTC branch only, int8-quantised and converted to ONNX.

## pyannote segmentation-3.0

Speaker segmentation — finds the stretches of audio containing one voice.

- **Publisher:** Hervé Bredin / pyannote
- **Upstream:** https://huggingface.co/pyannote/segmentation-3.0
- **Licence:** MIT.
- **Commercial use:** permitted. Note the upstream repository is access-gated:
  downloading from it requires a Hugging Face account and acceptance of its
  conditions. Aloudly obtains the model from the ungated ONNX conversion below.
- **Obtained from:** https://huggingface.co/csukuangfj/sherpa-onnx-pyannote-segmentation-3-0
- **Modifications:** ONNX conversion.
- **Citations requested by the model card:**
  - Plaquet, A. and Bredin, H. *Powerset multi-class cross entropy loss for
    neural speaker diarization* (2023).
  - Bredin, H. *pyannote.audio 2.1 speaker diarization pipeline: principle,
    benchmark, and recipe* (2023).

## NVIDIA NeMo TitaNet (small)

Speaker embedding extraction — decides which stretches of audio are the same
person. Also used for the optional local voice print.

- **Publisher:** NVIDIA Corporation
- **Upstream:** NVIDIA NeMo toolkit.
  https://docs.nvidia.com/nemo-framework/user-guide/latest/nemotoolkit/asr/speaker_recognition/models.html
- **Licence:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/),
  per NVIDIA's terms for the TitaNet checkpoints.
- **Commercial use:** permitted, with attribution.
- **Obtained from:** https://huggingface.co/csukuangfj/speaker-embedding-models
  (`nemo_en_titanet_small.onnx`)
- **Modifications:** ONNX conversion.
- **Reference:** Koluguri, N.R., Park, T., and Ginsburg, B. *TitaNet: Neural
  Model for Speaker Representation with 1D Depth-wise Separable Convolutions
  and Global Context* (2021).

> The source repository for this file carries no model card, so the licence
> above is taken from NVIDIA's terms for the TitaNet family rather than from
> the conversion itself.

---

## Speech engine

Model inference uses [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) by
the k2-fsa project, licensed under the Apache License 2.0.

## Redistribution

**This repository currently hosts no model files.** Every model listed above is
downloaded by Aloudly directly from the third-party source named in its
"Obtained from" line.

If a model file is published here as a release asset, its entry above must
record what was changed. In particular, a re-serialisation of Parakeet's
encoder into ONNX external-data form is a modification of CC BY 4.0 licensed
material and must be stated as such, alongside the attribution and licence link
already given.

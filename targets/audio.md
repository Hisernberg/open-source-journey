# Targets — Audio / Speech

Pick **2 primaries**. k2-fsa projects are famously newcomer-friendly; ESPnet gives research credibility.

| Repo | Why | First moves |
|---|---|---|
| **k2-fsa/sherpa-onnx** ⭐ primary | Next-gen Kaldi ecosystem; extremely welcoming; many languages/examples | example scripts, model export docs, small bugs |
| **k2-fsa/icefall** ⭐ | Training recipes (ASR/TTS/SSL) | recipe fixes, doc updates |
| **espnet/espnet** ⭐ | Research ASR standard, GSoC history | recipe fixes, docs, egs2 cleanups |
| speechbrain/speechbrain | Training toolkit | loss/recipe fixes, tests |
| librosa/librosa | Audio Python staple (NumFOCUS) | API edge cases, docs |
| NVIDIA/NeMo | Production ASR/TTS | imports, configs, docs |
| SYSTRAN/faster-whisper · m-bain/whisperX | Whisper ecosystem | VAD fixes, benchmarks, docs |
| idiap/coqui-ai-TTS | Community-maintained TTS fork (verify current home before working) | trainer fixes, docs |
| OHF-Myaic/piper (Piper TTS ecosystem) | Lightweight TTS | voice/scripts fixes — verify current repo |
| modelscope/FunASR | ASR toolkit | docs, small fixes |
| tobiasrapp/audiomentations (verify location) | Audio augmentation | transform tests |
| MTG/essentia | MIR (GSoC history) | C++ fixes, Python bindings |
| openai/whisper | Reference ASR | tokenizer/docs fixes (code is stable) |
| usefido/moonshine (verify current home) | Efficient ASR | docs, small fixes |

**Progression path:** docs/example scripts → onnx export fixes → one owned recipe/model export → large PR (new model export pipeline or a benchmark across runtimes).

**Maintenance-mode note:** torchaudio has announced a maintenance phase (2025) — still fine for small fixes; verify the current state before investing. coqui-ai/TTS (original) is archived — contribute to the maintained fork instead.

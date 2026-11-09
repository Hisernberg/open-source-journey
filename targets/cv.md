# Targets — Computer Vision

Pick **2 primaries + 2 secondaries**. OpenCV + scikit-image are the friendliest entry points.

| Repo | Why | First moves |
|---|---|---|
| **opencv/opencv** ⭐ primary | GSoC perennial; Python bindings + C++ core | tutorials, Python binding tests, tiny fixes |
| **scikit-image/scikit-image** ⭐ | NumFOCUS, kind reviewers, clean codebase | docstring polish → edge-case fixes → algorithm PRs |
| **albumentations-team/albumentations** ⭐ | Augmentation standard, fast reviews | transform bugs, new transforms + tests |
| kornia/kornia | Differentiable CV | loss modules, ops tests |
| huggingface/pytorch-image-models (timm) | Vision models hub | weight-conversion scripts, docs |
| pytorch/vision (torchvision) | Foundation | transforms, ops tests |
| google-ai-edge/mediapipe | Deployment | build fixes, example updates |
| open-mmlab/mmdetection et al. | Detection suites | config/bug fixes, deprecation cleanups |
| Project-MONAI/MONAI · MIC-DKFZ/nnU-Net · pydicom | Medical imaging (GSoC-adjacent) | dataset loaders, tests, docs |
| colmap/colmap · isl-org/Open3D · nerfstudio-org/nerfstudio | 3D vision / NeRF / Gaussian splatting | C++/CUDA fixes, docs |
| torchgeo/torchgeo | Geospatial ML | dataset additions |
| HumanSignal/label-studio · cvat-ai/cvat · Voxel51/fiftyone | Annotation tooling | UI/backend fixes |

**Progression path:** docs/tests → small algorithm fixes → one owned area (e.g. a transform family in albumentations) → large PR (new algorithm module with benchmark vs. reference implementation).

**Watchlist / verify current status:** Ultralytics (license/CLA considerations), Detectron2 (slowing), SAM-2 (research-code style), MediaPipe (active but C++ heavy).

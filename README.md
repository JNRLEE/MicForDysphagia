# MicForDysphagia

**Microphone-based dysphagia screening using swallowing acoustics**

> Full code and dataset will be released upon paper publication.

---

## What is this?

Dysphagia (swallowing disorder) affects a large portion of post-stroke and elderly patients, yet current clinical screening tools are either subjective (bedside questionnaires) or expensive and invasive (videofluoroscopic swallowing study). We are building a non-invasive, low-cost alternative using a contact microphone placed on the neck.

This repository documents the machine learning research pipeline for classifying swallowing sounds recorded with a neck-mounted microphone.

---

## Research Pipeline

```
Raw Audio (neck microphone)
        │
        ▼
  Preprocessing & Segmentation
  (noise gating, normalization, fixed-length windowing)
        │
        ▼
  Feature Extraction
  (MFCC, mel-spectrogram, energy envelopes,
   spectral statistics, WaveTokenizer embeddings)
        │
        ▼
  Classification Model
  (task: healthy vs. dysphagia; severity grading via EAT-10)
        │
        ▼
  Clinical Output
  (screening score, confidence, interpretability report)
```

---

## Dataset

- **Subjects**: 166+ patients (dysphagia confirmed via clinical evaluation) + normal controls
- **Recordings**: 1,600+ audio files across multiple swallowing tasks
- **Tasks**: dry swallow, water swallow (10 ml / 20 ml), jelly, cracker, resting baseline
- **Labels**: EAT-10 score, clinical assessment, selection type

> Patient data is not publicly available due to IRB restrictions.

---

## Current Status

| Component | Status |
|---|---|
| Data collection | Complete |
| Preprocessing pipeline | Complete |
| Feature extraction | Complete |
| Model training & validation | In progress |
| Paper submission | In preparation |

---

## Related Work

This project is part of a broader research program on acoustic-based swallowing assessment. A companion project ([SwallowSimulation3D](https://github.com/JNRLEE/SwallowSimulation3D)) develops 3D physics simulations of pharyngeal anatomy to generate synthetic training data and provide mechanistic insight into swallowing acoustics.

---

## Code Release

The full codebase, trained models, and evaluation scripts will be made publicly available upon acceptance of the accompanying paper. If you are interested in collaboration or early access, please open an issue or contact us directly.

---

## License

To be determined upon publication.

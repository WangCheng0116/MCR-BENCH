<div align="center">
    <h1>When Audio and Text Disagree: Benchmarking Text Bias in Large Audio-Language Models under Cross-Modal Inconsistencies</h1>


[![arxiv](https://img.shields.io/badge/Arxiv-2508.15407-b31b1b.svg?logo=arXiv)](https://arxiv.org/abs/2508.15407) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT) 
</div>

## 🎯 What this paper does
* **Introduces MCR-BENCH**, a benchmark of ~3k samples across Audio QA, Speech Emotion Recognition, and Vocal Sound Classification, explicitly pairing audio with **faithful, adversarial, and irrelevant** text.
* **Finds strong text bias**: when audio and text conflict, many LALMs overwhelmingly follow the text, causing severe accuracy drops on audio-centric tasks.
* **Analyzes causes & mitigations**: confidence calibration issues, representational separability of inconsistent inputs, limited gains from prompting, and partial improvements via supervised fine-tuning.

## 📂 Dataset Structure

```
MCR-BENCH/
├── AQA/
│   ├── AQA.json
│   └── audio/
├── SER/
│   ├── SER.json
│   └── audio/
└── VSC/
   ├── VSC.json
   └── audio/
```

Each JSON contains:
```json
{
  "audio": "path/to/audio.wav",
  "gt": "ground_truth", 
  "faithful": "accurate_description",
  "adversarial": "contradictory_description", 
  "irrelevant": "unrelated_description",
  "neutral": "question_without_description"
}
```

## 💾 Data release
📁 **Download**: [Google Drive Link](https://drive.google.com/file/d/1nXJCx8Neqdm0WMfe9Uq6sX2bvk_3FWUG/view?usp=sharing)

We don't provide evaluation code as each LALM requires separate complex setup (different components, dependencies, frameworks).

## 📖 Citation
If you find this paper useful, please consider citing our paper:
```bibtex
@misc{2508.15407,
   Author = {Cheng Wang and Gelei Deng and Xianglin Yang and Han Qiu and Tianwei Zhang},
   Title = {When Audio and Text Disagree: Revealing Text Bias in Large Audio-Language Models},
   Year = {2025},
   Eprint = {arXiv:2508.15407},
}
```

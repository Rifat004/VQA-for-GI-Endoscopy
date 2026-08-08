# Robust-VQA-for-GI-Endoscopy

This repository containes notebooks that containes fine-tuning and **robustness analysis** of Vision–Language Models (VLMs) for Visual Question Answering on gastrointestinal endoscopy images, built on the [Kvasir-VQA](https://huggingface.co/datasets/SimulaMet-HOST/Kvasir-VQA) dataset.

All experiments were conducted using **Python 3.12**. Several libraries can be installed using pip commands available in notebooks.

## Repository Structure

```
VQA-for-GI-Endoscopy/
├── Florence2-L/
│   └── Florence2-L.ipynb                                   # Full fine-tuning baseline
├── SmolVLM/
│   └── SmolVLM-QLoRA.ipynb                                 # QLoRA  (4-bit)
├── Qwen2.5VL/
│   └── Qwen2.5-VL_QLoRA.ipynb                              # QLoRA  (4-bit)
├── Idefics3/
│   ├── Idefics3_Augmentation(perturbed)-based-training.ipynb   #perturbation-based augmentation
│   └── Idefics3_Adversarial_training.ipynb                 # gradient-based adversarial training
├── PaliGemma2/
│   ├── PaliGemma2_Augmentation(clean10x)_based_training.ipynb      #clean 10x augmentation
│   ├── Paligemma2-Augmentation(perturbed)-based-training.ipynb     #perturbation-based augmentation
│   └── PaliGemma2_Adversarial-training.ipynb               # gradient-based adversarial training
├── mapped_q_endobench_kvasirvqa.csv                        # EndoBench ↔ Kvasir-VQA question mapping
├── requirements.txt
└── README.md
```


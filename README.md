# Robust-VQA-for-GI-Endoscopy

This repository containes notebooks that containes fine-tuning and **robustness analysis** of Vision–Language Models (VLMs) for Visual Question Answering on gastrointestinal endoscopy images, built on the [Kvasir-VQA](https://huggingface.co/datasets/SimulaMet-HOST/Kvasir-VQA) dataset. All experiments were conducted in jupyter notebooks.

## Repository Structure

```
VQA-for-GI-Endoscopy/
├── Florence2-L/
│   └── Florence2-L.ipynb                                           # Full fine-tuning baseline
├── SmolVLM/
│   └── SmolVLM-QLoRA.ipynb                                         # QLoRA  (4-bit)
├── Qwen2.5VL/
│   └── Qwen2.5-VL_QLoRA.ipynb                                      # QLoRA  (4-bit)
├── Idefics3/
│   ├── Idefics3_Augmentation(perturbed)-based-training.ipynb       # augmentation: 1x clean + 9x perturbed 
│   └── Idefics3_Adversarial_training.ipynb                         # gradient-based adversarial training
├── PaliGemma2/
│   ├── PaliGemma2_Augmentation(clean10x)_based_training.ipynb      #clean 10x augmentation
│   ├── Paligemma2-Augmentation(perturbed)-based-training.ipynb     # augmentation: 1x clean + 9x perturbed
│   └── PaliGemma2_Adversarial-training.ipynb                       # gradient-based adversarial training
├── mapped_q_endobench_kvasirvqa.csv                                # EndoBench ↔ Kvasir-VQA question mapping
├── requirements.txt
└── README.md
```

## Setup

```bash
git clone https://github.com/Rifat004/VQA-for-GI-Endoscopy.git
cd VQA-for-GI-Endoscopy

python3.12 -m venv .venv
source .venv/bin/activate          

pip install -r requirements.txt
```

**Core dependencies** (`requirements.txt`):

```
torch==2.9.0          torchvision==0.24.0
accelerate==1.12.0    peft==0.19.1
bitsandbytes==0.49.2  datasets==3.6.0
evaluate==0.4.6
```

Additional packages can be installed inside the notebooks with the pip commands available in notebooks.
# **🌱COPOTO Plant DX**

Predict Crop Type & Disease from Leaf Images

---

## **Overview**

This project uses a **single CNN** to predict both **crop type** (Tomato, Potato, Corn) and **disease** (e.g., Late Blight, Early Blight, Healthy) from leaf images. It’s designed to be **scalable, interpretable, and deployable**.

---

## **Features**

* Multi-task CNN with **crop head (auxiliary)** and **disease head (primary)**
* Handles **class imbalance** with weighted loss and balanced sampling
* **Grad-CAM visualizations** for interpretability
* **API-ready** for web or mobile apps
* Supports **LLM integration** for actionable guidance

---

## **Dataset Structure**

```
dataset_crop/
├── train/
│   ├── Tomato/
│   ├── Potato/
│   └── Corn/
├── val/
│   ├── Tomato/
│   ├── Potato/
│   └── Corn/
└── test/
    ├── Tomato/
    ├── Potato/
    └── Corn/
```

Labels CSV example:

| filename     | crop   | disease     | split |
| ------------ | ------ | ----------- | ----- |
| img\_001.jpg | Tomato | LateBlight  | train |
| img\_002.jpg | Potato | EarlyBlight | train |

---

## **Getting Started**

1. Clone the repo:

```bash
git clone https://github.com/username/multi-crop-cnn.git
cd multi-crop-cnn
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Prepare dataset (folder + CSV)
4. Train model and run inference

---

## **License**

MIT License

---

This is short, clear, and portfolio-friendly.

I can also **make an even snappier “1-minute read” version** suitable for GitHub’s front page if you want.

Do you want me to do that?

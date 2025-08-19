---

# 🌱 Multi-Crop Multi-Task CNN

**Predict Crop Type & Disease from Leaf Images**

---

## **Project Snapshot**

| Feature          | Description                                                               |
| ---------------- | ------------------------------------------------------------------------- |
| **Goal**         | Predict both crop and disease in a single CNN                             |
| **Crops**        | Tomato, Potato, Corn                                                      |
| **Diseases**     | Late Blight, Early Blight, Common Rust, Gray Leaf Spot, Healthy, etc.     |
| **Architecture** | Shared CNN backbone (ResNet/EfficientNet) with two heads (crop & disease) |
| **Deployment**   | API-ready, app integration, LLM-guided advice                             |

---

## **Why This Project?**

* **Unified multi-crop model** → fewer models to maintain
* **Multi-task learning** → predicts crop + disease simultaneously
* **Handles class imbalance** → weighted loss & balanced sampling
* **Interpretable** → Grad-CAM shows which leaf areas drive predictions
* **Real-world relevance** → helps smallholder farmers detect diseases early

---

## **Visual Pipeline**

```
[Leaf Image]
      │
      ▼
[CNN Backbone: ResNet/EfficientNet]
      │
 ┌────┴────┐
 │         │
Crop Head  Disease Head
(Aux)      (Primary)
 │          │
Crop Pred  Disease Pred
      │
      ▼
 Multi-Task Loss → Backprop
```

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

**Labels CSV (`labels.csv`)**

| filename     | crop   | disease     | split |
| ------------ | ------ | ----------- | ----- |
| img\_001.jpg | Tomato | LateBlight  | train |
| img\_002.jpg | Potato | EarlyBlight | train |

---

## **Getting Started**

1. **Clone Repo**

```bash
git clone https://github.com/username/multi-crop-cnn.git
cd multi-crop-cnn
```

2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

3. **Prepare Dataset**

   * Organize images by crop folder
   * Create CSV with disease labels & splits

4. **Train Model**

```python
# Load Dataset & Dataloader
# Initialize MultiTaskCNN
# Train with weighted multi-task loss: L_total = α*L_crop + β*L_disease
```

5. **Inference & Deployment**

* Predict crop + disease for new images
* Serve via FastAPI / Flask
* Optionally, connect to LLM for actionable guidance

---

## **Evaluation & Visualization**

* **Metrics:** Accuracy, F1-score per crop/disease
* **Visuals:** Confusion matrices, Grad-CAM attention maps
* **Comparisons:** Single-stage vs multi-task CNN

---

## **Social Impact**

* Empowers smallholder farmers with **real-time disease detection**
* Supports **food security** and **sustainable farming**
* Low-cost, scalable solution suitable for **low-resource settings**

---

## **Future Work**

* Add more crops & rare diseases
* Experiment with attention mechanisms / vision transformers
* Transfer learning across crops
* Integrate real-field images for robustness

---

## **Contact / Demo**

* GitHub: [Yusuf Abol](https://github.com/Yusuf-Abol)
* Demo app: Streamlit/Gradio coming soon

---

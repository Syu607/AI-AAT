# AI-AAT  
## 🍅 Tomato Leaf Disease Detection & Mobile Deployment

AI-AAT is a deep learning–based tomato leaf disease detection system designed with
**cross-domain robustness**, **explainable AI**, and **efficient mobile deployment**
in mind. The project demonstrates an end-to-end pipeline from model training to
offline Android deployment using **Flutter** and **ONNX Runtime**.

---

## 🔍 Key Features

- Multiclass tomato leaf disease classification  
- Cross-domain evaluation (lab → real-field images)  
- Multi-model comparison (DenseNet121 vs ResNet50)  
- Explainable AI using **Grad-CAM++** and **LIME**  
- ONNX export with **INT8 post-training quantization**  
- Offline Android deployment using **Flutter**  

---

## 📂 Dataset

This project uses **publicly available datasets** (not included in this repository):

### 🟢 Training Dataset
- **PlantVillage (Tomato subset)**
- Lab-controlled images
- Used for training and validation

### 🔵 Testing Dataset
- **TomatoVillage – Variant A (Multiclass Classification)**
- Real-field images
- Used for cross-domain evaluation

> ⚠️ Note: The TomatoVillage dataset contains only a subset of disease classes.
> Evaluation is therefore restricted to overlapping categories, following standard
> cross-domain evaluation practice.

---

## 🧠 Models

### 🔹 Primary Model (Deployed)
- **DenseNet121**
- Framework: PyTorch
- Selected due to better accuracy-to-parameter efficiency and stronger
  cross-domain generalization

### 🔹 Comparative Model
- **ResNet50**
- Used for architectural comparison and ablation analysis

---

## 🧪 Explainable AI (XAI)

Model decisions are interpreted using:

- **Grad-CAM++** – Visualizes spatial attention on diseased regions  
- **LIME** – Highlights superpixel-level feature contributions  

Explainability analysis confirms that the models focus on
**biologically relevant disease patterns**, improving trust and transparency.

---

## ⚙️ Optimization & Quantization

- Models exported to **ONNX format**
- **Static INT8 post-training quantization** applied using ONNX Runtime
- Achieved:
  - ~70% reduction in model size
  - Faster on-device inference
  - No retraining required

---

## 🚀 Deployment

- **Platform:** Android  
- **Framework:** Flutter  
- **Inference Engine:** ONNX Runtime Mobile  
- **Mode:** Fully offline, on-device inference  

Only the **best-performing DenseNet121 model** is deployed to ensure
lightweight and efficient mobile inference.

---

## 📊 Experimental Results (Summary)

- Cross-domain accuracy reflects realistic domain shift between lab and field images  
- Late blight shows stronger generalization due to distinctive visual characteristics  
- Explainable AI validates meaningful attention on disease-affected regions  
- INT8 quantization enables practical mobile deployment  

---

## 📘 How to Run

1. Open `notebooks/Tomato_Leaf_Disease.ipynb` in **Google Colab**
2. Train models and perform cross-domain evaluation
3. Generate XAI visualizations (Grad-CAM++ & LIME)
4. Export ONNX models and apply INT8 quantization
5. Deploy the model using the Flutter app in `flutter_app/`

---

## 📁 Repository Structure

AI-AAT/
│
├── notebooks/
│ └── Tomato_Leaf_Disease.ipynb
│
├── flutter_app/
│ └── Flutter mobile application
│
├── deployment/
│ ├── densenet121_fp32.onnx
│ └── densenet121_int8.onnx
│
└── README.md


---

## 👨‍🎓 Author

**Mohammed Sulaiman**  
M.Tech. Computer Science & Engineering  
Interests: Deep Learning, Computer Vision, Explainable AI, Mobile AI Deployment

---

## 📄 License

This project is intended for **academic and research purposes**.
Please cite the original datasets and libraries used.

# AI-AAT

# 🍅 Tomato Leaf Disease Detection

This project presents a deep learning-based tomato leaf disease detection system
with cross-domain robustness and mobile deployment using Flutter and ONNX Runtime.

## 🔍 Features
- Multiclass tomato leaf disease classification
- Cross-domain evaluation (lab → field images)
- ONNX export and INT8 quantization
- Offline Android deployment using Flutter

## 📂 Dataset
- PlantVillage (training)
- TomatoVillage Variant-A (testing)

Datasets are publicly available and not hosted in this repository.

## 🧠 Model
- Backbone: DenseNet121
- Framework: PyTorch
- Optimization: INT8 ONNX Quantization

## 🚀 Deployment
- Platform: Android
- Framework: Flutter
- Runtime: ONNX Runtime Mobile

## 📊 Results
- High classification accuracy
- Reduced model size (~70%)
- Fast on-device inference

## 📘 How to Run
1. Open `notebooks/Tomato_Leaf_Disease.ipynb` in Google Colab
2. Train and export ONNX models
3. Deploy using Flutter app in `flutter_app/`

## 👨‍🎓 Author
Mohammed Sulaiman 

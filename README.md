AI-AAT
🍅 Tomato Leaf Disease Detection & Mobile Deployment

AI-AAT is a deep learning–based tomato leaf disease detection system designed with
cross-domain robustness, explainable AI, and efficient mobile deployment
in mind. The project demonstrates a complete pipeline—from model training and
cross-domain evaluation to lightweight deployment on Android using
Flutter and ONNX Runtime.

🔍 Key Features

Multiclass tomato leaf disease classification

Cross-domain evaluation (lab → real-field images)

Multi-model comparison across four CNN architectures

Explainable AI using Grad-CAM++ and LIME

Teacher–student knowledge distillation

ONNX export and deployment-ready optimization

Offline Android deployment using Flutter

📂 Dataset

This project uses publicly available datasets (not included in this repository).

🟢 Training & Validation Dataset

PlantVillage (Tomato subset) - https://drive.google.com/drive/folders/1k8c0JN8MuEaO2NBkmddOeCabceAAPDE3?usp=drive_link

Laboratory-controlled images

10 disease/healthy classes

Split: 80% training, 20% validation

🔵 Cross-Domain Testing Dataset

TomatoVillage – Variant A (Multiclass Classification) - https://drive.google.com/drive/folders/1CVdBAzweB_xR7qUm5RcM3HJ71ZPrZn5N?usp=drive_link

Real-field images captured under natural conditions

Used only for testing

⚠️ Note: TomatoVillage contains additional field-condition classes.
Cross-domain evaluation is restricted to overlapping categories
(Early Blight, Late Blight, Healthy) to ensure label consistency.

🧠 Models
🔹 Teacher Models (Training & Analysis)

The following architectures were trained using transfer learning and evaluated
for cross-domain robustness:

DenseNet121

DenseNet201

ResNet101

EfficientNet-B4

Among these, DenseNet121 achieved the best cross-domain performance.

🔹 Student Model (Deployed)

MobileNetV3 (Lightweight CNN)

Trained using knowledge distillation from the teacher ensemble

Optimized for mobile inference

Exported and deployed in ONNX format

🧪 Explainable AI (XAI)

Model predictions were interpreted using:

Grad-CAM++ – Visualizes spatial attention on disease-affected regions

LIME – Highlights superpixel-level feature contributions

Explainability was applied to teacher models to verify that predictions
focus on biologically relevant leaf regions.
The deployed student model operates in ONNX format, where gradient-based XAI
is not supported.

⚙️ Optimization & Deployment

Student model exported to ONNX

Designed for:

Reduced model size

Faster inference

Offline execution

Deployment stack:

Flutter (mobile UI)

ONNX Runtime Mobile (inference engine)

This enables fully offline tomato leaf disease detection on Android devices.

📊 Experimental Results (Summary)

Cross-domain accuracy is significantly lower than in-domain accuracy,
highlighting real-world challenges

DenseNet121 showed the strongest generalization across domains

Late Blight exhibited higher robustness due to distinctive visual patterns

Knowledge distillation produced a lightweight student model suitable for deployment

Explainable AI confirmed meaningful attention on diseased regions

📘 How to Run

Open notebooks/Tomato_Leaf_Disease.ipynb in Google Colab

Train teacher models and perform cross-domain evaluation

Apply explainable AI (Grad-CAM++ and LIME)

Train and export the student model using knowledge distillation

Export ONNX models for deployment

Deploy using the Flutter application in flutter_app/

📁 Repository Structure
AI-AAT/
│
├── notebooks/
│   └── Tomato_Leaf_Disease.ipynb
│
├── models/
│   ├── teacher_models/
│   └── student_model/
│
├── deployment/
│   └── student_shufflenetv3.onnx - https://drive.google.com/file/d/1cbqBkrPozowQceDxYO9DGSWBYJtNx7D8/view?usp=drive_link
│
├── flutter_app/
│   └── Android mobile application
│
└── README.md

👨‍🎓 Author

Mohammed Sulaiman
M.Tech – Computer Science & Engineering

Interests:
Deep Learning, Computer Vision, Explainable AI, Mobile AI Deployment

📄 License

This project is intended for academic and research purposes only.
Please cite the original datasets and libraries used.

🎓 One-Line Project Summary

An explainable, cross-domain tomato leaf disease detection system with a deployed student model optimized for offline mobile inference.

# 🌱 AI-Based Smart Plant Disease Monitoring System

**An AI-powered plant health monitoring system integrating Deep Learning, Computer Vision, Explainable AI (XAI), and Internet of Things (IoT).**

---

## 📌 Project Overview

Plant diseases are one of the major factors affecting crop health and agricultural productivity. Traditional disease identification methods primarily depend on manual inspection, which can be time-consuming and may require expert knowledge.

The **AI-Based Smart Plant Disease Monitoring System** aims to provide an automated and intelligent approach to plant health monitoring by combining deep learning-based disease classification with IoT-enabled environmental sensing.

The proposed system uses an **ESP32-CAM** to capture plant leaf images and environmental sensors to monitor temperature, humidity, and soil moisture. A **MobileNetV2-based deep learning model** is used to identify possible plant diseases from leaf images.

To improve the interpretability of the model, **Grad-CAM (Gradient-weighted Class Activation Mapping)** is incorporated to visualize the regions of the leaf that influence the model's prediction.

Unlike systems that perform only one-time disease classification, the proposed system also focuses on continuous plant monitoring and recovery assessment. After providing suitable action or recovery guidance, the plant is monitored periodically to determine whether its condition is improving or the problem is persisting.

The overall objective is to develop a low-cost and practical prototype for intelligent plant disease detection, explainable analysis, environmental monitoring, and recovery tracking.

---

## 🎯 Project Objectives

- Develop an AI-based system for identifying plant diseases from leaf images.
- Implement MobileNetV2 for plant disease classification.
- Train and compare multiple deep learning architectures to evaluate their classification performance.
- Integrate Grad-CAM to provide visual explanations of model predictions.
- Implement an ESP32-CAM-based image acquisition system.
- Monitor environmental parameters such as temperature, humidity, and soil moisture.
- Provide suitable action and recovery guidance based on the identified plant condition.
- Implement periodic monitoring to assess whether the plant is recovering or its condition is persisting.
- Integrate the AI model, embedded hardware, and monitoring system into a working prototype.

---

## 💡 Key Features

| Feature | Description |
|---|---|
| Plant Disease Detection | Identifies possible plant diseases from leaf images using deep learning. |
| MobileNetV2 Classification | Uses MobileNetV2 as the baseline disease classification model. |
| Model Comparison | Evaluates multiple deep learning architectures using consistent performance metrics. |
| Explainable AI | Uses Grad-CAM to highlight important regions influencing predictions. |
| Image Acquisition | Captures plant images using ESP32-CAM. |
| Environmental Monitoring | Measures temperature, humidity, and soil moisture. |
| Recovery Monitoring | Periodically evaluates changes in the plant's condition. |
| Action Guidance | Provides suitable guidance based on the identified condition. |

---

## 🏗️ System Architecture

The proposed system consists of the following major stages:

1. **Image Acquisition:** ESP32-CAM captures images of plant leaves.
2. **Environmental Data Collection:** Sensors collect temperature, humidity, and soil moisture readings.
3. **Image Preprocessing:** Captured images are resized and prepared for model input.
4. **Disease Classification:** MobileNetV2 analyzes the leaf image and predicts the plant condition.
5. **Explainable AI:** Grad-CAM generates heatmaps highlighting the regions responsible for the prediction.
6. **Action Guidance:** Suitable guidance is provided based on the identified plant condition.
7. **Recovery Monitoring:** New images and environmental readings are collected periodically and compared with previous observations.

### System Workflow

```text
          PLANT
            |
            v
       ESP32-CAM
            |
            v
      IMAGE CAPTURE
            |
            v
    IMAGE PREPROCESSING
            |
            v
     MOBILENETV2 MODEL
            |
            v
    DISEASE CLASSIFICATION
            |
            v
         GRAD-CAM
            |
            v
     VISUAL EXPLANATION
            |
            v
     ACTION GUIDANCE
            |
            v
    RECOVERY MONITORING
            |
            v
     PERIODIC OBSERVATION
            |
            v
    IMPROVING / PERSISTING
```

Environmental sensors continuously provide additional information about the plant's surrounding conditions.

---

## 🧠 Deep Learning Models

MobileNetV2 is selected as the baseline architecture for plant disease classification because of its lightweight design and suitability for image classification tasks.

Additional deep learning architectures will be trained and evaluated to compare their performance against the baseline model.

### Model Evaluation

The models will be evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Training and Validation Loss
- Training and Validation Accuracy
- Inference Time

The final model selection will be based on experimental results and suitability for the proposed system.

---

## 🔍 Explainable AI – Grad-CAM

Grad-CAM is used to improve the interpretability of the disease classification model.

Instead of displaying only the predicted disease class, Grad-CAM produces a visual heatmap showing the regions of the leaf that contributed to the model's prediction.

This helps users understand which visual features influenced the classification.

The generated heatmap is overlaid on the original leaf image to produce an interpretable visualization.

---

## 🔌 Hardware Components

The proposed hardware prototype consists of the following components:

| Component | Purpose |
|---|---|
| ESP32-CAM | Captures plant leaf images. |
| DHT22 Sensor | Measures temperature and humidity. |
| Capacitive Soil Moisture Sensor | Measures soil moisture levels. |
| 0.96-inch OLED Display | Displays relevant system information. |
| Buzzer and LEDs | Provides visual and audible indications. |
| Breadboard | Supports circuit connections. |
| Jumper Wires | Connects the electronic components. |
| USB Cable / Power Supply | Provides power to the prototype. |

---

## 💻 Technologies Used

### Software and Programming

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

### Artificial Intelligence

- Deep Learning
- Convolutional Neural Networks (CNN)
- MobileNetV2
- Transfer Learning
- Grad-CAM
- Image Processing

### Embedded Systems and IoT

- ESP32-CAM
- Arduino IDE
- DHT22
- Capacitive Soil Moisture Sensor
- OLED Display

---

## 📂 Repository Structure

```text
AI-Based-Smart-Plant-Disease-Monitoring-System/
│
├── 01_Dataset/
│   ├── raw/
│   ├── processed/
│   ├── train/
│   ├── validation/
│   ├── test/
│   ├── train.csv
│   └── dataset_description.md
│
├── 02_Data_Preprocessing/
│   ├── image_preprocessing.py
│   ├── dataset_splitting.py
│   ├── data_augmentation.py
│   ├── dataset_visualization.py
│   └── class_distribution.py
│
├── 03_Model_Training/
│   ├── MobileNetV2/
│   ├── Model_2/
│   ├── Model_3/
│   ├── Model_4/
│   ├── Model_5/
│   └── compare_models.py
│
├── 04_Model_Evaluation/
│   ├── evaluate_model.py
│   ├── confusion_matrix.py
│   ├── classification_report.py
│   ├── plots/
│   └── comparison_results/
│
├── 05_Explainable_AI/
│   ├── gradcam.py
│   ├── heatmap_generation.py
│   ├── visualization.py
│   └── sample_outputs/
│
├── 06_Deployment/
│   ├── model_conversion/
│   ├── inference/
│   └── api_or_interface/
│
├── 07_Hardware_ESP32/
│   ├── ESP32_CAM/
│   ├── DHT22/
│   ├── Soil_Moisture/
│   ├── OLED_Display/
│   ├── Integration/
│   └── circuit_diagram.png
│
├── 08_Recovery_Monitoring/
│   ├── recovery_tracking.py
│   ├── recommendation_system.py
│   └── condition_assessment.py
│
├── 09_Documentation/
│   ├── synopsis.pdf
│   ├── project_presentation.pdf
│   ├── project_architecture.md
│   ├── hardware_setup.md
│   └── model_training_guide.md
│
├── 10_Notebooks/
│   ├── 01_dataset_exploration.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_mobilenetv2_training.ipynb
│   ├── 04_model_comparison.ipynb
│   └── 05_gradcam.ipynb
│
├── 11_Results/
│   ├── training_curves/
│   ├── confusion_matrices/
│   ├── gradcam_results/
│   └── model_comparison.csv
│
├── 12_Tests/
│   ├── test_preprocessing.py
│   ├── test_inference.py
│   └── test_model_loading.py
│
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
└── CONTRIBUTING.md
```

*Note: Large datasets, trained model weights, and other generated artifacts may be maintained separately using appropriate storage or versioning tools.*

---

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ramsey-06/AI-Based-Smart-Plant-Disease-Monitoring-System.git
```

### 2. Navigate to the Project Directory

```bash
cd AI-Based-Smart-Plant-Disease-Monitoring-System
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Environment

**Windows:**

```bash
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
source .venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Project Implementation Workflow

The project is organized into the following development stages:

| Stage | Implementation |
|---|---|
| Stage 1 | Dataset collection and exploration |
| Stage 2 | Image preprocessing and augmentation |
| Stage 3 | MobileNetV2 baseline model training |
| Stage 4 | Training and comparison of additional models |
| Stage 5 | Model evaluation and performance analysis |
| Stage 6 | Grad-CAM implementation |
| Stage 7 | ESP32-CAM and sensor integration |
| Stage 8 | Plant recovery monitoring |
| Stage 9 | Complete prototype testing |

Detailed implementation instructions will be maintained in the respective repository folders.

---

## 📊 Results and Performance Analysis

Experimental results will be added after model training and prototype testing.

The following results will be documented:

- Dataset distribution and preprocessing results.
- Training and validation accuracy.
- Training and validation loss.
- Model-wise performance comparison.
- Confusion matrices.
- Classification reports.
- Grad-CAM visualizations.
- Hardware testing results.
- System response and recovery monitoring observations.

### Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| MobileNetV2 | TBD | TBD | TBD | TBD |
| Model 2 | TBD | TBD | TBD | TBD |
| Model 3 | TBD | TBD | TBD | TBD |
| Model 4 | TBD | TBD | TBD | TBD |
| Model 5 | TBD | TBD | TBD | TBD |

*Performance values will be updated after experimental evaluation.*

---

## 🌿 Applications

- Smart agriculture.
- Greenhouse monitoring.
- Home gardening.
- Plant nurseries.
- Small-scale farming.
- Precision agriculture.
- Automated plant health assessment.

---

## ⭐ What Makes This Project Different?

Many plant disease detection systems focus primarily on classifying a leaf image and providing a disease prediction.

The proposed system aims to extend this functionality by integrating:

1. Deep learning-based disease classification.
2. Visual explanation of predictions using Grad-CAM.
3. Environmental monitoring through IoT sensors.
4. Suitable action and recovery guidance.
5. Periodic plant monitoring to assess changes in plant condition.

By combining these features, the project aims to provide a more comprehensive plant health monitoring solution rather than performing only one-time disease classification.

---

## ⚠️ Limitations

- Disease classification performance depends on the quality and diversity of the training dataset.
- Predictions may be affected by lighting, background, image quality, and real-world environmental conditions.
- Grad-CAM provides a visual explanation of model attention but does not independently establish a biological diagnosis.
- Recovery assessment requires consistent periodic observations.
- Hardware and deployment performance must be validated through prototype testing.

The system is intended as a decision-support tool and should not replace expert agricultural diagnosis.

---

## 👩‍💻 Project Contributors

**Department of Electronics and Communication Engineering**

**BMS College of Engineering, Bengaluru**

**Academic Year: 2026–2027**

| Name | USN |
|---|---|
| Aditya N | 1BM24EC006 |
| B S Amrutha Varshini | 1BF24EC040 |
| Chinmayi M | 1BF24EC047 |
| Dhakshi Priya S | 1BF24EC053 |

**Project Guide:** Prof. K Poornima Kamath

**Mini Project:** 23EC5PWMPR

---

## 📚 References

1. S. Janarthan, S. Thuseethan, S. Rajasegarar and J. Yearwood, "P2OP—Plant Pathology on Palms: A Deep Learning-Based Mobile Solution for In-Field Plant Disease Detection," *Computers and Electronics in Agriculture*, Vol. 202, 2022. DOI: [10.1016/j.compag.2022.107371](https://doi.org/10.1016/j.compag.2022.107371).

2. M. Shoaib et al., "An Advanced Deep Learning Models-Based Plant Disease Detection: A Review of Recent Research," *Frontiers in Plant Science*, Vol. 14, 2023. DOI: [10.3389/fpls.2023.1158933](https://doi.org/10.3389/fpls.2023.1158933).

3. S. Natarajan, P. Chakrabarti and M. Margala, "Robust Diagnosis and Meta Visualizations of Plant Diseases Through Deep Neural Architecture with Explainable AI," *Scientific Reports*, Vol. 14, 2024. DOI: [10.1038/s41598-024-64601-8](https://doi.org/10.1038/s41598-024-64601-8).

4. "Exploring Explainable AI Techniques for Plant Disease Classification in Digital Agriculture," *Procedia Computer Science*, Vol. 265, 2025. DOI: [10.1016/j.procs.2025.07.170](https://doi.org/10.1016/j.procs.2025.07.170).

5. N. Ibnat et al., "Artificial Intelligence in Modern Agriculture: Recent Advances, Challenges, and Future Directions: A Systematic Review," *Artificial Intelligence in Agriculture*, 2026. DOI: [10.1016/j.aiia.2026.08.005](https://doi.org/10.1016/j.aiia.2026.08.005).

---

## 📄 License

This project is developed as an academic mini-project at BMS College of Engineering.

The licensing terms for the source code, dataset, and other third-party resources should be respected. Refer to the repository's LICENSE file for applicable permissions.

---

**Made with 🌱 by the Project Team**

*AI-Based Smart Plant Disease Monitoring System | BMSCE | 2026–2027*

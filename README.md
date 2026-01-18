# Breedify – Intelligent Cattle Breed Classification System

Breedify is a deep learning–based computer vision project designed to automatically identify cattle and classify their breeds from images.
The system uses a two-stage model pipeline to improve accuracy, efficiency, and scalability, making it suitable for real-world livestock management and agri-tech applications.

🚀 Project Overview

Breedify works in two sequential stages:

Model_A (Cattle vs Non-Cattle Detection)
Filters input images to determine whether they contain cattle or not.

Model_B (Cattle Breed Classification)
Once an image is confirmed as cattle, it is passed to a multi-class model that classifies the cattle into one of 35 different breeds.

Both models are trained using EfficientNet (EfficientNet-B series) for high performance with optimized computational cost.

**🧠 Why Two Models?**

Using a two-model pipeline offers several advantages:

1.Prevents non-cattle images from entering the breed classifier
2. Improves overall accuracy
3.Faster and more efficient inference

🔄 Easier future expansion (adding new breeds or animal types)

**📂 Dataset Structure**
Dataset for Model_A (Binary Classification)
dataset_model_A/
│
├── cattle/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
│
└── non_cattle/
    ├── img1.jpg
    ├── img2.jpg
    └── ...


Classes:

cattle

non_cattle

Dataset for Model_B (Breed Classification – 35 Classes)
dataset_model_B/
│
├── Gir/
├── Sahiwal/
├── Red_Sindhi/
├── Tharparkar/
├── Holstein_Friesian/
├── Jersey/
├── ...
└── (Total: 35 breed folders)


Each folder contains images of a specific cattle breed.

**🏗️ Model Architecture
**
Base Model: EfficientNet (pretrained on ImageNet)

Framework: TensorFlow / Keras

Transfer Learning: Yes

Fine-Tuning: Applied for better domain adaptation

Model_A

Binary classification (cattle vs non_cattle)

Softmax / Sigmoid output

Model_B

Multi-class classification (35 breeds)

Softmax output layer

🛠️ Technologies Used

Python 🐍

TensorFlow & Keras

EfficientNet

NumPy

OpenCV

Matplotlib

Scikit-learn

🔄 Workflow

Input image

Image passed to Model_A

If output = cattle → forward to Model_B

Model_B predicts the cattle breed

Final prediction displayed

**📈 Key Features
**
✔️ High accuracy with EfficientNet
✔️ Modular two-model design
✔️ Scalable to more breeds

separation

**🌱 Future Scope
**
1.Mobile/Web app integration
.Real-time camera-based prediction
3.IoT integration for smart farms
4.Blockchain-based cattle identity tracking
5.Expansion to other livestock (buffalo, goats, etc.)
✔️ Real-world agriculture & livestock use case

✔️ Clean dataset separation

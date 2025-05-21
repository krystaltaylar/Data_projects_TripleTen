# 🧑‍💻 Age Estimator: Facial Age Prediction with Deep Learning

## 📍 Project Description

This project was developed for **Good Seed**, a supermarket chain exploring the use of computer vision to comply with alcohol laws by verifying customers’ ages at checkout. The goal was to build a deep learning model that could estimate a person’s age from a photo, using real-world images captured by checkout cameras.

---

## 📑 Table of Contents

- [Technologies and Tools Used](#technologies-and-tools-used)  
- [Project Structure](#project-structure)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)  
- [Conclusion](#conclusion)  
- [Suggestions for Business Improvement](#suggestions-for-business-improvement)  

---

## 🛠️ Technologies and Tools Used

- Python  
- TensorFlow / Keras  
- ResNet50  
- Pandas  
- Matplotlib  
- ImageDataGenerator  

---

## 🧭 Project Structure

- **Data Loading:**  
  Loaded 7,591 face images and corresponding ages from CSV and image files.

- **Exploratory Data Analysis (EDA):**  
  - Visualized the distribution of real ages.  
  - Found that the dataset skewed younger, with a median age of 29.  
  - Maintained outliers (like 100-year-olds) to keep data diverse.

- **Image Preprocessing:**  
  - Rescaled pixel values to [0, 1] using `ImageDataGenerator`.  
  - Resized all images to 224x224 to match the ResNet50 input shape.

- **Model Architecture:**  
  - Used **ResNet50** (pre-trained on ImageNet) as the base.  
  - Added a Global Average Pooling layer and two dense layers with dropout.  
  - Output layer had one unit for age prediction (regression).

- **Model Training:**  
  - Loss function: Mean Squared Error (MSE)  
  - Metric: Mean Absolute Error (MAE)  
  - Optimizer: Adam with learning rate 0.0001  
  - Trained on GPU for 20 epochs with a batch size of 32

---

## ⚙️ Setup Instructions
- Clone repository to your local machine and install dependencies using pip install.

---

## 🚀 Usage

Run the notebook `Age_Estimator.ipynb` to:

- Load and preprocess image data  
- Explore the dataset visually and statistically  
- Build and compile the CNN model (using ResNet50 as base)  
- Train and evaluate the model  
- Analyze model performance using MAE  

---

## 🧾 Conclusion

The model successfully estimated human age from face images with a **test MAE of ~7.65**, which meets the goal of keeping error below 8 years.

### 🔍 Key Observations:

- Training MAE improved steadily from **7.4 to 3.1**  
- Validation MAE fluctuated, peaking at **epoch 12**, but ultimately improved  
- Slight overfitting was observed, indicated by the gap between train and validation MAE  

Despite these challenges, the model performed well and is suitable for use in age-verification applications.

---

## 💡 Suggestions for Business Improvement

- **Real-time integration:** Deploy the model with camera input for real-time age verification at checkout.  
- **Threshold classification:** Use predicted age ranges to trigger manual ID checks (e.g., flag anyone estimated under 25).  
- **Bias review:** Assess demographic balance in images to reduce prediction bias.  
- **Model refinement:** Consider using additional facial attributes or ensemble models to reduce MAE further.

# Cat vs Dog Classifier (CNN + Flask)

## Overview

This project is a **Deep Learning-based web application** that classifies images as **Cat 🐱 or Dog 🐶** using a Convolutional Neural Network (CNN).

It includes:

* A trained CNN model
* A Flask backend for inference
* A frontend UI for image upload

---

## Features

* Upload any image of a cat or dog
* Real-time prediction using trained model
* Simple and interactive UI
* REST API-based backend

---

## Model Details

* Input size: **128 × 128 × 3**
* Architecture:

  * 3 Convolutional layers
  * MaxPooling layers
  * Dense layers with Dropout
* Output: Binary classification (Cat / Dog)

---

## Dataset

* ~25,000 images used for training
* Images stored and processed using NumPy & Pickle
* Data normalized (pixel values scaled between 0 and 1)

---

## Tech Stack

### Backend

* Flask
* TensorFlow / Keras
* NumPy
* PIL

### Frontend

* HTML
* CSS
* JavaScript

---

## Project Structure

```id="9k3xq1"
├── predictor_model.h5      # Trained CNN model
├── app.py                 # Flask backend
├── index.html             # Frontend UI
├── style.css              # Styling
├── script.js              # Frontend logic
├── cat_image.png          # UI asset
├── dog_image.png          # UI asset
```

---

## How It Works

1. User uploads an image from the frontend
2. Image is sent to Flask API (`/predict`)
3. Image is preprocessed:

   * Resized to 128×128
   * Normalized
4. Model predicts:

   * `0 → Cat`
   * `1 → Dog`
5. Result is displayed on UI

---

## Run Locally

### 1. Clone the repository

```bash id="8a2kdl"
git clone https://github.com/yourusername/cat-vs-dog-classifier.git
cd cat-vs-dog-classifier
```

### 2. Install dependencies

```bash id="1s9xpl"
pip install flask flask-cors tensorflow numpy pillow
```

### 3. Run the Flask server

```bash id="0l2mwe"
python app.py
```

### 4. Open frontend

* Open `index.html` using Live Server (VS Code recommended)

---

## API Endpoint

### POST `/predict`

**Input:**

* Form-data with key `image`

**Output:**

```json id="p7d4we"
{
  "prediction": 0
}
```

* `0 → Cat 🐱`
* `1 → Dog 🐶`

---

## 📷 UI Preview

* Upload image
* Click submit
* Get prediction instantly

---

## 📌 Future Improvements

* Add probability/confidence score
* Improve model accuracy
* Deploy using Render / AWS / Vercel
* Add drag-and-drop upload
* Support more animal classes

---

## 👨‍💻 Author

**Sanat Naik**

* GitHub: https://github.com/sanatNaik
* Email: [sanatnaik2005@gmail.com](mailto:sanatnaik2005@gmail.com)

---

## ⭐ Contribution

Feel free to fork and improve the project!

---

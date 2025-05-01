
# Real-Time DeepFake Detection System

A Flask-based web application that allows users to upload an image and instantly detect whether it is a deepfake or real using a pre-trained deep learning model.

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Flask](https://img.shields.io/badge/Flask-WebApp-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🔍 Features

- 🧠 **Deepfake Detection**: Classifies uploaded images as "Real" or "Fake" with a confidence score.
- ⏱️ **Real-Time Processing**: Fast predictions using MobileNet-based CNN.
- 🔐 **Rate Limiting**: Restricts uploads to 5 per minute using Redis.
- 🖼️ **Image Support**: Accepts `.jpg`, `.jpeg`, `.png` formats.
- 🌐 **Responsive UI**: Clean, mobile-friendly interface built with HTML & CSS.
- ⚙️ **Flask Backend**: Lightweight Python web framework.

---

## 📁 Project Structure

```
deepfake/
│
├── app.py                   # Flask backend application
├── templates/
│   └── index.html           # Web interface
├── uploads/                 # Stores uploaded images temporarily
├── deepfake_model.pkl       # Pre-trained deepfake detection model
├── requirements.txt         # List of dependencies
└── README.md                # Project documentation
```

---

## ⚙️ Technologies Used

- **Flask** – Web application framework
- **TensorFlow** – For loading and predicting with deepfake model
- **MobileNet** – Lightweight CNN used as the backbone
- **Redis** – Rate limiting backend
- **Pillow (PIL)** – Image handling
- **NumPy** – Image preprocessing
- **Werkzeug** – Secure file uploads

---

## 🚀 Getting Started

### 🔧 Prerequisites

Install Python dependencies:
```bash
pip install -r requirements.txt
```

Start Redis server (for rate-limiting):
```bash
redis-server
```

---

### ▶️ Run the App

```bash
python app.py
```

Visit the web app at:  
```
http://127.0.0.1:5000/
```

---

## 📸 Usage

1. Upload an image (.jpg/.jpeg/.png).
2. Click **Detect**.
3. See the classification result and confidence score.
4. Limited to 5 uploads per minute per user.

---

## 📊 Model Details

- **Model File**: `deepfake_model.pkl`
- **Input Size**: 224x224 pixels
- **Architecture**: MobileNet with a dense classifier
- **Threshold**: Confidence > 0.7 → Real, otherwise Fake

---

## ⚠️ Limitations

- Only works for **images**, not videos.
- Accuracy depends on dataset quality.
- May misclassify very subtle manipulations.

---

## 🛠️ Future Improvements

- 🔁 Video deepfake detection
- 🎨 Better UI/UX experience
- 🧪 Larger and more diverse datasets
- ☁️ Cloud deployment (e.g., Heroku/Render)

---

## 📚 References

- Dataset: [Deepfake Detection Dataset – Kaggle](https://www.kaggle.com/datasets)
- Book: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* by Aurélien Géron

---

## 📄 License

This project is under the [MIT License](LICENSE).

---

## 🤝 Contributing

Found a bug or have an idea?  
Feel free to [open an issue](https://github.com/KZV027/Real-Time-DeepFake-Detection/issues) or submit a PR!

---

## 👤 Author

**Kshitiz Verma** 
**Kritika Singh** 
B.Tech CSE | Babu Banarasi Das University  
GitHub: [KZV027](https://github.com/KZV027)
Github: [Kritka2121](https://github.com/Kritika2121)


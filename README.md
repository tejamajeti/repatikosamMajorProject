🩺 Skin Disease Predictor
A Flask + React application that predicts skin diseases from uploaded images using a Deep Learning model.

📌 Features
✅ Upload an image (JPG, JPEG, PNG)
✅ AI-based prediction of skin diseases
✅ Top 4 conditions with probability scores
✅ Simple, user-friendly UI

📂 Project Structure
📦 Skin-Disease-Predictor
├── 📁 backend (Flask Server)
│   ├── app.py  # Flask API for prediction
│   ├── skin_disease_model_ISIC_densenet.h5  # Trained deep learning model
│   ├── requirements.txt  # Python dependencies
│   ├── static/images/  # Uploaded images storage
│   ├── templates/  # HTML templates (if used)
│   └── ...  
├── 📁 frontend (React App)
│   ├── src/App.js  # Main React file
│   ├── src/index.js  # React entry point
│   ├── public/  # Static files
│   ├── package.json  # React dependencies
│   └── ...


🚀 Setup Guide
1️⃣ Install Dependencies
📌 Backend (Flask)
pip install -r requirements.txt
📌 Frontend (React)
npm install
2️⃣ Start the Flask Server
python app.py
Runs on: http://localhost:4000/
Endpoints:
POST /predict → Uploads image and gets prediction
3️⃣ Start the React App
npm start
Runs on: http://localhost:3000/
Interacts with Flask API for predictions
🛠 API Usage
🔹 Endpoint: POST /predict
Request:
Content-Type: multipart/form-data
Body:
file: Upload an image (JPG, PNG)
Response:
json
Copy
Edit
{
  "class1": "Benign keratosis",
  "prob1": 91.05,
  "class2": "Atopic Dermatitis",
  "prob2": 1.88,
  "class3": "Vascular lesion",
  "prob3": 1.76,
  "class4": "Melanocytic nevus",
  "prob4": 1.62,
  "image_url": "/static/images/filename.jpg"
}


📌 Tech Stack
🔹 Backend: Flask, TensorFlow/Keras
🔹 Frontend: React, Axios
🔹 Model: DenseNet-based Skin Disease Classification

🎯 Future Improvements
✅ Deploy using Docker
✅ Add more skin disease categories
✅ Improve model accuracy
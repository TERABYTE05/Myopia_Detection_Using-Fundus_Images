👁️ Myopia Detection From Fundus Images

A classical machine-learning pipeline for detecting Myopia from retinal fundus images using handcrafted image features and a Random Forest classifier.

🏆 Achieved 97.50% accuracy on 2000 real fundus images

🏷️ Tech Stack

🐍 Python

☁️ Google Colab

👁️ OpenCV

📊 NumPy / Pandas

🧠 Scikit-Learn

🧵 Scikit-Image

📈 Matplotlib

🎯 Objective

Detect whether a retinal fundus image belongs to a Myopic or Normal eye using classical ML + image processing (no deep learning).

📂 Dataset Structure
eye_images/
├── myopic/
└── normal/


Description

myopic/ → Myopic retina images

normal/ → Normal retina images

Dataset is loaded from eye_images.zip stored in Google Drive.

📊 Features Used
Category	Feature Names
Intensity	Brightness, Contrast
Color	Mean R, G, B, Red-Green ratio, Red-Blue ratio
Texture	Shannon Entropy
Structure	Canny Edge Count
Sharpness	Laplacian Variance (Blurriness)

🧮 Total features: 10

⚙️ Pipeline
Load Images 
→ Extract Features 
→ Train/Test Split 
→ Random Forest 
→ Evaluation 
→ Predict New Images

✅ Model Results

🎯 Accuracy: 97.50%

🌲 Model: Random Forest (100 trees)

Metric	Score
Precision	98%
Recall	97–98%
F1-Score	97–98%
Confusion Matrix
	Pred Normal	Pred Myopic
Actual Normal	194	7
Actual Myopic	3	196
📈 Visual Outputs
File	Meaning
assets/myopic_hist.png	Histogram for myopic fundus image
assets/normal_hist.png	Histogram for normal fundus image
assets/avg_hist_myopic.png	Avg histogram (1000 myopic images)
assets/avg_hist_normal.png	Avg histogram (1000 normal images)
assets/pipeline.png	ML pipeline diagram
assets/test_prediction.png	Output example

✅ Images auto-generated when running the notebook

🚀 How to Run
1️⃣ Mount Drive
from google.colab import drive
drive.mount('/content/drive')

2️⃣ Place Dataset

Upload eye_images.zip to:

/content/drive/My Drive/eye_images.zip

3️⃣ Train the Model

Run the notebook cells for feature extraction + training.

4️⃣ Predict a New Image
result = predict_image("test_fundus.png")
print(result)  # Myopic / Normal

📦 Dependencies
opencv-python
numpy
pandas
matplotlib
scikit-learn
scikit-image
tqdm


Install manually (if needed):

pip install opencv-python scikit-image tqdm

🧪 Notes

✅ No deep learning — explainable ML

✅ CPU-friendly & lightweight

✅ Suitable for early-stage fundus analysis

🔮 Future Enhancements
Feature	Status
CNN / RETFound comparison	🔜
Streamlit Web App	🎨 Planned
Mobile app (TFLite)	📱 Future
Clinical dataset validation	🏥 Research stage
📜 License

MIT License — free to use & modify

✨ Credits

Developed by Teesha
AI assistance for formatting only

🙌 Support

If you like this project, please ⭐ the repo. It helps others find it!

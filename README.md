# Dynamic ASL Project

## Problem Definition
In remote work environments, individuals who are deaf or hard of hearing often face challenges in effectively communicating during video conferences. To address this, we propose a solution that leverages sign language recognition technology to break communication barriers and empower individuals with hearing impairments to communicate seamlessly.

## Project Goal
This project focuses on developing a real-time sign language recognition model that converts sign language into spoken language, facilitating seamless communication and creating new opportunities for individuals with hearing impairments. Beyond enabling communication, this solution unlocks new possibilities. For instance, it empowers deaf individuals to interact directly with clients using sign language in face-to-face services, such as banking.

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

## Workflow Diagram
![Workflow Diagram](https://github.com/user-attachments/assets/fe060caf-9f19-4ea1-a7b8-f9b9c1041e5f)
Step 1: Model Training
Step 2: Real-time Inference


## Project File Structure
The repository contains the following files and folders:
- **Data**      
  To use the project, you need to download the required data:
  1. Preprocessed Training Data (X_train.pkl and y_train.pkl)      
     Download the preprocessed training data from Google Drive:      
     📂 https://drive.google.com/drive/folders/1sS9uR_TRqf-w1lfazqaPGbcNhsTJyBIu?usp=drive_link      
  2. Original Dataset      
     The original dataset can be downloaded from Kaggle:                  
     📂 https://www.kaggle.com/datasets/risangbaskoro/wlasl-processed      
- **asl_top3_accuracy_model.h5**  
  Trained LSTM model with high accuracy.  
- **video_to_training_data.ipynb**  
  Jupyter notebook to process videos into training data (`X_train.pkl` and `y_train.pkl`).  
- **asl_top3_accuracy_model.ipynb**  
  Jupyter notebook for training and evaluating the LSTM model.

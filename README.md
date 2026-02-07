🧠 Face Verification System using Siamese Neural Network

A deep learning–based Face Verification System built with TensorFlow, Keras, and OpenCV.  
This model uses a Siamese Network to compare two facial images and determine if they belong to the same person.


🚀 Project Overview

This project demonstrates a real-time face verification approach using a webcam feed and a trained Siamese network.  
Instead of classifying identities, it learns similarity between faces by comparing embeddings.

Key Highlights:
1. Siamese Network architecture for one-shot learning 
2. Built using TensorFlow 2.x and Keras Functional API  
3. Includes a custom L1 distance layer for feature comparison  
4. Uses OpenCV for real-time webcam verification  
5. Trains on anchor, positive, and negative image triplets  

Project Structure:
- application_data/
	- input_image/          (single-frame captures used for verification)
	- verification_images/  (saved images used for verification testing)
- data/
	- anchor/               (anchor images for training)
	- positive/             (positive examples — same person)
	- negative/             (negative examples — different person)
- lfw/                    (optional LFW dataset folders)
- training_checkpoints/   (saved checkpoints during training)
- siamesemodelv2.h5       (example pretrained model)
- Face Verification.ipynb (notebook for collection, training, verification)

⚙️ Setup Instructions

 1. Clone the repository

git clone https://github.com/100376-govind/Face-Verification.git
cd Face-Verification


 2. Install dependencies

pip install tensorflow opencv-python numpy matplotlib


 3. Prepare dataset
Create directories for anchor, positive, and negative images

Use the webcam collection script in the notebook:
1. Press ‘a’ → Capture anchor image  
2. Press ‘p’ → Capture positive image  
3. Press ‘q’ → Quit capture  

 4. Train the model
(a) Run all notebook cells sequentially to:
1. Preprocess and augment data  
2. Build the Siamese embedding and distance models  
3. Train for a desired number of epochs  
4. Save the trained model  

(b) To perform real-time verification:
1. Press ‘v’ to verify the current webcam frame  
2. Press ‘q’to quit  



 🧠 Model Architecture

The Siamese Network includes:
1. Embedding Network – A CNN that converts face images into 4096-dimensional embeddings.  
2. L1 Distance Layer – Computes the absolute difference between embeddings.  
3. Dense Layer – Outputs a similarity score (0–1) via sigmoid activation.



 📊 Training Details

| Parameter | Value |
|------------|--------|
| Input size | 100 × 100 × 3 |
| Loss | Binary Crossentropy |
| Optimizer | Adam (1e-4) |
| Metrics | Precision, Recall |
| Epochs | 50 |


 🎯 Results

The model achieves high verification accuracy on unseen pairs.  
It performs robustly in real-time tests with variations in lighting and expression.


 🧰 Technologies Used
1. Python 3.10.10 
2. TensorFlow / Keras  
3. OpenCV  
4. NumPy  
5. Matplotlib  

 👨‍💻 Author

Govind Raj Gupta 
🔗 [GitHub Profile](https://github.com/100376-govind)
🔗 Video Link (https://www.linkedin.com/posts/govind-raj-gupta-415958324_machinelearning-deeplearning-ai-activity-7364625473420541952-zGIG?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFICuVEBqhjVnWnfD7O4BvQ1NCwm9N_zhug)

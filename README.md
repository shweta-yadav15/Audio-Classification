# Audio-Classification with Convolutional Neural Networks and Transfer Learning
Classifying sounds from real world environment into their respective categories.

## Problem Statement

The goal is to recognize sounds from a wide range of real-world environments. It is an audio classification problem.
The task is essentially to extract features from the audio, and then identify which class the audio belongs to. 
Many useful applications pertaining to audio classification can be found in the wild – such as intelligent domestic 
assistants, urban planning against noise pollution, etc.

---

## Dataset
ESC-50 or dataset for Environmental Sound Classification is used. It is a labeled collection of 2000 environmental audio recordings. 
It consists of 5-secong long recordings organized into 50 classes with 40 examples per class. All the sound clips are in .wav format
along with a csv file that contains original category of each audio and other information.
Link to dataset: https://github.com/karolpiczak/ESC-50

---

## Models Used

1. Model with raw waveforms and 1D convolutions
2. Model with relevant features extracted from audio data
3. Model build with transfer learning from images to audio data 

---
## Results
- Baseline Model: The model with raw waveforms after running for 500 epochs with batch size 32 gave an accuracy of 82% for training data and
46% for test data which is clearly a case of overfitting. 
- Model with raw waveforms is not giving outputs as expected. I am not sure what can be the reason.
- For model 2 performance is better. After running for 150 epochs with 256 batch size, the training data 
accuracy is 97% and test data is 58%. Here also we can observe overfitting but better than baseline model. 
--- 

## Tools Used
Keras API is used for major part of the project on top of TensorFlow along with few other libraries like NumPy, Pandas, Scikit-Learn and Librosa. Librosa is a python package widely used for audio and music processing. It allows to load audio in the notebook as a NumPy array for analysis and manipulation. Librosa’s load() function is used for much of the preprocessing. The advantage of using it is that it converts the sampling rate to 22.05kHz by default as well as normalize the data so the bit-depth values are in range [-1,1].

# Decoding EEG signals for BCI applications 

This was a learning project given by a company. Each task is written in a google colab notebook with concise code and detailed annotations. Data is hidden due to copyright.

## Task 1: Binary classification of SSVEP response based on focused flickering stimuli
EEG signals were segmented into epochs based on the onset of a flickering stimuli (7 Hz, 8.25 Hz, 10 Hz, 12 Hz) and the time of user-confirmed focused stimuli. Following that, machine learning algorithm was applied to classify the eeg segments according to the user-confirmed stimuli class. 

The following steps were covered in the google colab:
1. Import Libraries
2. Creating dataset from files
3. Signal processing
   - Notch filter: To filter out 60 Hz powerline noise
   - Bandpass filter: To select frequency of interest (1 Hz - 40 Hz)
   - Wavelet Transform Denoising: to remove noise in time-frequency domain
4. Feature Extraction
   - Linear Envelope + Root Mean Square
   - Continous Wavelet Transform (CWT)
   - Fast Fourier Transform (FFT) statistics
   - Discrete Wavelet Transform (DWT) Statstics
   - FFT statistics + Entropy
   - All above features combined
5. Feature Selection: PCA
6. Machine Learning Classification
   - Support Vector Machine (SVM) model
   - Multilayer Perceptron Model
7. Conclusions


## Task 2: Detecting P300 peak from stimuli 1 (std) & stimuli 2 (odd)
EEG signals were segmented into 800 ms epochs based on two of stimuli: standard (event_id = 1) and odd (event_id = 2). The P300 peaks were observed greatly from the odd stimuli response and their amplitudes and latency values were recorded. The following steps were covered:

1. Import Libraries
2. Creating dataset from files
3. Signal processing: Data imputation, Baseline correction, Notch filter, Bandpass filter, Wavelet transform Denoising 
4. Creating averaged single trial dataset (stimuli 1 & 2)
5. Creating averaged trials dataframe from all trials (stimuli 1 & 2)
6. Detecting P300 peak from average singal trial epochs data and average epochs data
7. Observations/Improvements

## Task 3: Detecting VEP peak from 15 Hz flickering stimuli 
EEG signals were segmented into 300 ms epochs based on a stimuli at event_id = 3. The VEP peaks were observed and their amplitudes and latency values were recorded. The following steps were covered:

1. Import Libraries
2. Creating dataset from files
3. Signal processing: Data imputation, Baseline correction, Notch filter, Bandpass filter, Wavelet transform Denoising 
4. Creating averaged single trial dataset (event_id = 3)
5. Creating averaged trials dataframe from all trials
6. Detecting VEP peak from average singal trial epochs data and average epochs data
7. Observations/Improvements

## Task 4: Binary classification of fatigue and no-fatigue response from EMG segments
EEG signals were segmented into 0.5 s epochs and caregorized into 'fatigue' and no-fatigue' class based on the mode of the class in the particular segment. Following that, machine learning algorithm was applied to classify the eeg segments and test it on unseen data. The following steps were covered:

1. Import Libraries
2. Creating dataset from files
3. Signal processing: Notch filter, Wavelet transform denoising, Band-pass filtering
4. Feature Extraction
   - Linear Envelope + Root Mean Square
   - Continous Wavelet Transform (CWT)
   - Fast Fourier Transform (FFT) statistics
   - Discrete Wavelet Transform (DWT) Statstics
   - FFT statistics + Entropy
   - Time domain and other statistics
   - All above features combined
5. Feature Selection: PCA
6. Machine Learning Classification
   - Support Vector Machine (SVM) model
   - Multilayer Perceptron Model
7. Conclusions



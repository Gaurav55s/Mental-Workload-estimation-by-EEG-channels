# Mental-Workload-estimation-by-EEG-channels
This repository presents estimation of mental workload in a normal human being by EEG signals and by applying Classification algorithms of Machine Learning.

The data has been taken from 'PhysioNet' (website : https://physionet.org/).

Data : https://physionet.org/content/eegmat/1.0.0/

Data description : The EEGs were recorded monopolarly using Neurocom EEG 23-channel system (Ukraine, XAI-MEDICA). The silver/silver chloride electrodes were placed on the scalp according to the International 10/20 scheme. All electrodes were referenced to the interconnected ear reference electrodes.

In this study, artifact-free EEG segments lasting 60 seconds each were utilized. Data preprocessing involved employing Independent Component Analysis (ICA) to remove artifacts such as those caused by eye movements, muscle activity, and cardiac interference (e.g., pulsations). A high-pass filter with a cut-off frequency of 30 Hz and a power line notch filter (50 Hz) were applied during preprocessing.

During the experimental task, participants engaged in an arithmetic task involving serial subtraction of two numbers. Each trial began with orally presented 4-digit (minuend) and 2-digit (subtrahend) numbers (e.g., 3141 and 42).

Participants meeting eligibility criteria had normal or corrected-to-normal visual acuity, normal color vision, and no clinical signs of mental or cognitive impairment, verbal or non-verbal learning disabilities. Exclusion criteria included the use of psychoactive medications, substance addiction, and psychiatric or neurological disorders.

Step-1 Raw data was downloaded and converted into CSV files. The data was then preprocessed. Preprocessing steps involved applying a bandpass filter 0.5Hz to 45Hz, re-referencing and removal of artifacts through Independent Component Analysis (ICA) The code has been given in 'Preprocessing.ipynb'.

Step-2 The preprocessed data was then imported for feature extraction. Complete visualisation of the data has been performed. Power Spectral Density of each channel has been drawn. Theta / alpha bandpower is calculated as the feature. The code has been given in 'Feature extraction.ipynb'

Step-3 The dataset consisting of all frontal chanels' (Fp1, Fp2, F3, F4, F7, F8, Fz) PSDs and Load was formed. The splitting if data into training and testing sets was done. Different classification algorithms were applied and score of each model was obtained. Classification algorithms used are :- KNN, Linear Regression, Ridge Regression, Logistic Regression, Gaussian Naive Bayes, Linear SVM, Decision Tree Classifier.

# Emotion-classification in EEG Signals:

EEG Dataset:
The DEAP dataset comprises EEG and peripheral physiological signals for 32 subjects who individually watched 40 one-minute music videos of different genres as a stimulus to induce different affective and emotional states. Within the dataset 32 channels were used to record EEG signals for each trial per subject, resulting in 8064 samples that represent the signal over each one-minute trial. During each trial, a single subject rated his/her feelings after watching the video using the Self Assessment Manikin (SAM) scale in the range [1-9] to indicate the associated levels of Valence, Arousal, Dominance, and Liking.

Data preprocessing and feature extraction:
I used the preprocessed EEG data provided by the DEAP dataset in Matlab and Python (numpy) format. The preprocessing operation includes data downsampled to 128Hz, EOG removal, filtering, segmentation, and so on. By using the preprocessed data provided by the DEAP dataset, we can avoid the problem of inconsistency of the evaluation criteria caused by the inconsistency of the preprocessing method, so as to reflect the value of the model better.

In this project, Fast Fourier transform (FFT) based power spectral density (PSD) was used as a feature. More specifically, signals are divided into five frequency band, Theta (4-7Hz), Alpha (8-12 Hz), Lower Beta (13-21Hz), Upper Beta (22-30 Hz) and Gamma (30-45Hz) and energy within each subband was summarized and used as features. The features from the same channel are concatenated into a vector, then the 2D feature can be constructed.

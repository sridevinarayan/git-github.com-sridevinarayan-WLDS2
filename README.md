#WLDS
# Steps:###
Data***
data/WAV contains all the audio samples used. The file naming convention is used to label the samples.
data/out contains the outputs generated.
    1. dataset_1.csv - got from extracting features from .WAV files
    2. .png files are the plots for the fitted model - for different test splits and #epochs
    3. results_0 and metrics_0
***

1. Prep.ipynb - to figure out which features need to be extracted. Experiements are done with several parameters
        a) On one sample hardcoded data file, data_21_FD.wav, extract different features
        b) MFCC (Mel-Frequency Cepstral Coefficients), Zero-crossing rate, Energy, Spectral-roll off, Spectral entropy  
2. Features.ipynb - to create a dataset by extracting features of the audio files (.WAV)
        a) Each audio file is manually labelled (filename) on what the file is
        b) all the files are read and features extracted and saved in a dataset.  
        c)Output: out_file_path = '/Users/ns/development/iisc/WLDS2/data/out/dataset_1.csv' 
3. train_fit_predict.ipynb - train the model and evaluate the predictions
        a) Read the extracted features from the  dataset
        b) Check the distribution of data
        c) Create a NN model
        d) split the data in different proportions (train_test_split)
        d) Fit and train the model for differnt epochs and for the different test proportions
        e) Analyse the accuracy and loss for the different sets






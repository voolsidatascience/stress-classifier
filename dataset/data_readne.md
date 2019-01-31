# Data Information

The original data comes from a project conducted at MIT by [Healey as a part of her PhD thesis](https://dspace.mit.edu/handle/1721.1/9067), and consist of body measurements conducted on various young people driving in stressing environments, e.g. rush hour, highways, red lights, as well as a relaxation period to create a non-stressed base reading. The dataset is freely available from [Physionet](https://www.physionet.org/tutorials/hrv/) 
The dataset is in a physionet specific format divided into 18 .dat files and 18 .hea files with accompanying meta data. The data consists signals for ECG, EMG, GSR measures from the foot, GSR measures from the hand, HR and Respiration. All values are float values, with a sampling frequency of 15.5 samples per second. The WFDB command rdsamp from the native terminal installation of Physionets tools named WFDB is used to read the data (Moody, 2015), then they are merged and saved as .txt files with column names, the measurement unit and the time in seconds for each row – including the data samples. The header names are manually cleaned and then the data is stored in a Pandas dataframe. Each file contains a sampling time starting at zero and stopping at the end of the sampling session. The time interval is incremented based on the last time interval of the previous file to transform the data into one continuous time-series. 

The raw data extracted into .txt files in this project can be accessed from here:
 https://1drv.ms/f/s!ApqYcVCNnKvChu1oGea_4JOPRfdOlA

- dataframe_hrv.csv
  - Feautere expanded version of the original dataset. The RR intervals have been converted into HRV featueres based on 30 seconds worth of samples
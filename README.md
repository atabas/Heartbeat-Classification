# Heartbeat Classification
## Classify ECG heartbeat signals into predefined categories based on heartbeat abnormality by transforming time series to images

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/ecg-heartbeat-classification-a-deep/myocardial-infarction-detection-on-ptb)](https://paperswithcode.com/sota/myocardial-infarction-detection-on-ptb?p=ecg-heartbeat-classification-a-deep)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/ecg-heartbeat-classification-a-deep/arrhythmia-detection-on-mit-bih-ar)](https://paperswithcode.com/sota/arrhythmia-detection-on-mit-bih-ar?p=ecg-heartbeat-classification-a-deep)

### Datasets:
- MIT-BIH Dataset (https://www.physionet.org/content/mitdb/1.0.0/): contains 5 categories: N, S, V, F, Q (see https://arxiv.org/pdf/1805.00794.pdf for details), 87k train records, 21k test records
- PTB Dataset (https://www.physionet.org/content/ptbdb/1.0.0/): contains 2 categories: Normal and Abnormal, 14k records

ECG heartbeat signals are time series data (187 signals per heartbeat in the given data)

![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/example_images.png "GAF, RP, MTF")

Approaches:
- Gramian Angular Field (GAF)
- Recurrence Plot (RP)
- Markov Transition Field (MTF)
- Intermediate fusion


![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/GAF+RP.png "GAF+RP")
![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/Fusion.png "Intermediate Fusion")
![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/GAF+RP+MTF.png "GAF+RP+MTF")


![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/results_mit_bih.png "Results for MIT BIH")
![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/Screenshots/results_ptb.png "Results for PTB")



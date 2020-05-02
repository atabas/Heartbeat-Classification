# Heartbeat Classification
## Classify ECG heartbeat signals into predefined categories based on heartbeat abnormality by transforming time series to images

### Datasets:
- MIT-BIH Dataset (https://www.physionet.org/content/mitdb/1.0.0/): contains 5 categories: N, S, V, F, Q (see https://arxiv.org/pdf/1805.00794.pdf for details), 87k train records, 21k test records
- PTB Dataset (https://www.physionet.org/content/ptbdb/1.0.0/): contains 2 categories: Normal and Abnormal, 14k records

ECG heartbeat signals are time series data (187 signals per heartbeat in the given data)

![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/data_example.png "GAF and RP")

### Gramian Angular Field (GAF)
- Image obtained from a time series representing the temporal correlation between each time point. 
- Normalize time series (n points) to [-1, 1]
- Construct (n x n) matrix by taking dot product of every 2 elements
- Project these to a 2D space to obtain an angular distance measurement between every 2 points. Details here: https://medium.com/analytics-vidhya/encoding-time-series-as-images-b043becbdbf3 

### Recurrence Plot
Based on the recurrent behaviour of time series.
In our case, it is implemented by:
- Taking pairwise euclidean distances of the n time points, giving us an (n x n) matrix
- Clipping the max distance by some max threshold (10)
- Normalizing the values in [-1,1]

![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/architecture.png "Network Architecture")

![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/results_mit-bih.png "Results for MIT BIH")
![alt text](https://github.com/atabas/Heartbeat-Classification/blob/master/results_ptb.png "Results for PTB")



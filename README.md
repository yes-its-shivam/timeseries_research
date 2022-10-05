# gtmhub_timeseries
This respository is created inorder to implement nbeats algorithm introduced in [Neural Basis Expansion Analysis For
Interpretable Time Series](https://arxiv.org/pdf/1905.10437.pdf) with RevIN normalisation introduced in [Reversible Instance Normalisation For
Accurate Time-Series Forecasting Against
Distribution Shift](https://openreview.net/pdf?id=cGDAkQo1C0p).

## ABSTRACT

### N-BEATS ALGORITHM:
> Nbeats architecture design methodology relies on a few key principles. First, the base architecture
should be simple and generic, yet expressive (deep). Second, the architecture should not rely on timeseries-specific feature engineering or input scaling. These prerequisites let us explore the potential
of pure DL architecture in TS forecasting. Finally, as a prerequisite to explore interpretability, the
architecture should be extendable towards making its outputs human interpretable. We now discuss
how those principles converge to the proposed architecture.

### RevIN:
> In this technique a new reversible instance normalization technique is introduced to alleviate the distribution shift problem in
time-series, which is known to cause a substantial discrepancy between the training and test data
distributions

### Model Architectures:
>[Nbeats Only Architecture](https://github.com/yes-its-shivam/gtmhub_timeseries/blob/main/nbeats.png) | [Nbeats+RevIN Architecture](https://github.com/yes-its-shivam/gtmhub_timeseries/blob/main/nbeats-revin.png)


### Benchmarks
| SNo. | N-Beats | Nbeats+RevIN | Facebook Prophet |
| --- | --- | --- | --- |
| 1 | .... | .... | .... |
| 2 | .... | .... | .... |
| 3 | .... | .... | .... |
| 4 | .... | .... | .... |
| 5 | .... | .... | .... |
| 6 | .... | .... | .... |
| 7 | .... | .... | .... |
| 8 | .... | .... | .... |
| 9 | .... | .... | .... |
| 10 | .... | .... | .... |


### QUICK START

#### Dependencies
```
!git clone https://github.com/yes-its-shivam/gtmhub_timeseries.git
%cd gtmhub_timeseries
!pip install -r requirements.txt
```
##### In the nbeats-revin-forecast.py define the location to your .csv file
```
df = pd.read_csv(YOUR FILE PATH HERE, parse_dates = ['timestamp'], index_col = 'timestamp')
# sort by dates
df.sort_index(inplace = True)
df.drop('Unnamed: 0',axis=1,inplace=True)
```

### Conclusions:

* The combined model is performing better for dataset with less amount of randomness
   * for dataset with more randomness either we need more data or we can try implementing nbeats with ensembling combined with RevIN
* Overall performance of the combined model is better then just nbeats model
* Overall performance
      

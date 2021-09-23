# Gartex Timeseries Forcasting

In this project I tried to learn hidden patterns in 5 timeseries signals and forecast their future; Then I designed an anomaly detection system for these signals.

## Getting Started

You can clone or download this project as zip file. You shoud open html file if you want see the results but if you want to contribute you'd better run the ipynb file with jupyter notebook.

### Prerequisites

You have to install jupyter notebook for ipynb file and an internet browser for html file.

## Running the tests

Run all cells in jupyter notebook. You can see results by analyzing 2 plots showing forecast of future with real signal and showing anomaly signal.

### Break down into end to end tests

The first plot shows forecast future of last 30% of data with the real data. The second one shows the anomalis of signal according to the real value and forecast.

## Built With

* [Jupyter Notebook](http://www.https://jupyter.org/) - The notebook used
* [Python](https://https://www.python.org/) - Language used

## Report

The first step is to import libraries needed. Our dataset is a time series signal of number of units produced in different parts of a production line. CID determines section of production line and quantity shows number of units built in that time stamp. Our data is clean and does not need any preprocess. The first row seems to have a wrong timestamp so i removed it fram dataset. I used groupby to check distribution of data amongst CIDs and it is clear that the ones with most data are CID 18 and 60. The next step is to divide dataset into 5 signals, one for each CID. I faced so many problems while implementing learning methods on this signal and the reason was high number of samples without usefull information so i used a sample of signal instead of its original form. I picked 1 row in every 25 row and as you could see below the general form of time serie did not change at all. In the next step i used a an ARIMA model on the time series and predicted unknown values of last 30% of data with this model. Now I used some statistical concepts and found anomalies with their intensity and taged the highest intensity as anomaly. About 10% of data is labeled as anomaly. I created a signal for anomaly which is 1 when it is anomaly and 0 when it is not. I also implemented a LSTM model and got the results but they were not as good as ARIMA model. Although I think I can work on this model and make it better.

## Authors

* **Omid Vaheb** - *Initial work* - [Virasad](https://gitlab.virasad.ir/o.vaheb/gartx-forecasting)
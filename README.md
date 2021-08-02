# Stock Price Predictor with HeadlineMove
---
## Project of Finance 2nd Team in Insight, the party gathered to study data science

### Project Topic
__Stock price prediction modeling for short-term investment using LSTM and Headline Move__

__I was involved in data preprocessing, modeling, error correction formula development, and code refactoring.__

### Engineering Environment
module|version
---|---
Python|3.8
TensorFlow|2.3.1
Gensim|3.8.3
Pandas|1.2.0
Numpy|1.19.2
FinanceDataReader|0.9.10

---
### Directory
```
+--data
      +--headline
      +--train_test
      +--vector
+--model
+--scaler
      +--train_scaler
```
directory name|description
---|---
headline|This directory contains all Headline data
train_test|This directory contains test data used to measure model performance
vector|This directory contains sumed 100d vectorized Headline data
model|This directory contains Word2Vec model and LSTM model
scaler|This directory contains MinMaxScaler of sklearn

### Methology
![image](https://user-images.githubusercontent.com/48271454/105496468-d9c6ce00-5d00-11eb-933c-0c7bc1210e22.png)

---

### Graph of loss
![image](https://user-images.githubusercontent.com/48271454/105496356-b6038800-5d00-11eb-97dd-031d662c6f8e.png)

### Error Correction

We did error corrction. Because we do not have enough data, so model shows over 3% error when using MAPE metric.

In addition, the goal of our project is not to predict an increase or decrease, but to precisely match the stock's next day's open, high, low, and close prices.

To achieve the goal, we made an assumption that the error of the previous day and that of the next day would be similar,
because they both use almost the same data, and we made a formula. The formula is as follows.

![image](https://user-images.githubusercontent.com/48271454/105497547-58703b00-5d02-11eb-83c2-8325a2d02e3c.png)

As shown in the table below, after calibration, we were able to obtain better model performance.

![image](https://user-images.githubusercontent.com/48271454/105499335-aa19c500-5d04-11eb-9b81-b4a5bb7df201.png)

### Prediction graph after correction
![image](https://user-images.githubusercontent.com/48271454/105498259-493dbd00-5d03-11eb-81ad-b5bb034f937f.png)

---
### Limitation

We only trained two years of data from the semiconductor, pharmaceutical (bio) and telecommunications industries. In this industry, the model seems to predict somewhat closer (since previous studies have focused on binary predictions such as increase or decrease, this also has no clear criterion), but it is vulnerable to rapid increases and decreases, and similar prediction performance is shown in other industries. I can't guarantee.

---
### Link of Full Report
https://www.notion.so/Report-7d7ce5d00c724849971fbab40a6ccb63

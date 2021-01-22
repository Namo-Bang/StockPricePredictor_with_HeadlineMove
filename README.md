# Stock Price Predictor with HeadlineMove
---
## Project of Finance 2nd Team in Insight, the party gathered to study data science

### Project Topic
__Stock price prediction modeling for short-term investment subsidies using LSTM and Headline Move__

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
__Directory__
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

#### Methology
![image](https://user-images.githubusercontent.com/48271454/105496117-6624c100-5d00-11eb-90ca-38054dee804c.png)


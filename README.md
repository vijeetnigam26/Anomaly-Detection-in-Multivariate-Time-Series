<h2 align="center"> 🕵🏻Anomaly Detection in 📈Multivariate ⏳Time-Series </h2>

<p align="center">
  <img src="https://www.datarobot.com/wp-content/uploads/2020/06/Introducing-Automated-Time-Series-Anomaly-Detection_blog_Image_v.1.0.png" height=55% width=55% />
</p> 

•	Detected Data Anomalies/Outliers in 3 different Multivariate Time Series Data Sets related to [**Health Care**](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-ecg-autoencoders), [**Tourism**](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-expedia-hotel), and [**Transportation Sectors**](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-sensors-var).

•	Implemented and Compared **ANN, VAR, Isolation forests, K-Means Clustering, PCA,** and **SVM** to get the best model accuracy.

•	Built an efficient Autoencoders Model with an accuracy of **94.96%**.

•	Applied Neural Networks and Deep Learning Methods for detecting anomalies.


📒 **Do Checkout my Kaggle Notebooks**

- [Anomaly Detection in Multivariate Time-Series](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-in-multivariate-time-series)
- [Anomaly Detection: ECG - Autoencoders](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-ecg-autoencoders)
- [Anomaly Detection: Expedia Hotel](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-expedia-hotel)
- [Anomaly Detection: Sensors - VAR](https://www.kaggle.com/code/vijeetnigam26/anomaly-detection-sensors-var)

<h2> Problem Statement 1: ECG</h2>

**The objective of detecting anomalies in ECG signals consists of finding the irregular heart rates, heartbeats, and rhythms. To achieve this goal, an anomaly detection system must be able to find them on all heartbeat sequences; therefore, to obtain the essential metrics.**

An electrocardiogram (ECG) is a simple test that can be used to check your heart's rhythm and electrical activity. Sensors attached to the skin are used to detect the electrical signals produced by your heart each time it beats.

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/ecg.webp" height=55% width=55% />
</p> 

<h3> 🥅 Autoencoders</h3>

Autoencoder is an important application of Neural Networks or Deep Learning. It is widely used in dimensionality reduction, image compression, image denoising, and feature extraction. It is also applied in anomaly detection and has delivered superior results.

Autoencoders are a specific type of feedforward neural network.

It consists of two parts:-
1.Encoder
2.Decoder

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/autoencoders1.png?raw=true" height=60% width=60% />
</p> 

👉🏻 *In simple words, AutoEncoder is an unsupervised Artificial Neural Network that attempts to encode the data by compressing it into the lower dimensions (bottleneck layer or code) and then decoding the data to reconstruct the original input. The bottleneck layer (or code) holds the compressed representation of the input data.*

This model was just the basic model and it can be improved by doing hyperparameter tuning and making the encoder and decoder with DNN. The threshold was determined using a very simple method and it can be also changed for getting better and more accurate results. The criteria for determinig the threshold can make a lot of difference.

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/accuracy.png?raw=true" height=80% width=80% />
</p> 

<h3></h3>

<h2> Problem Statement 2️: Expedia Hotel</h2>

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/expedia.png" height=55% width=55% />
</p> 

The [**Dataset**](https://www.kaggle.com/datasets/vijeetnigam26/expedia-hotel/versions/1) is related to tourism sector and is multivariate, dependent on time series. The main objective here is to check and observe the hotel prices from the data set of expedia hotel search. I have implemented different models here to check the prices hikes and lows. 

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/expedia_search.webp" height=80% width=80% />
</p> 

<h3> 📊 Techniques </h3>

Based on this study, we have observed that Algorithms - **K-Means**, **3D Clusters**, **PCA**, **Isolation Forest**, and **Gaussian Distribution** have detected the high prices.
<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/svm.png" height=55% width=55% />
</p> <br>

But only **One Class SVM** has detected both high prices as well as low prices.

**❓ BUT.. How one class svm made such difference?**

SVM is for novelty detection, a max-margin methods, i.e. they do not model a probability distribution... The idea of novelty detection is to detect rare events, i.e. events that happen rarely, and hence, of which you have very little samples.

<h2> Problem Statement 3️: Sensors</h2>

<p align="center">
  <img src="https://github.com/vijeetnigam26/Anomaly-Detection-in-Multivariate-Time-Series/blob/master/img/sensors1.webp" height=55% width=55% />
</p> 

Detect the outliers/anomalies in the experimental dataset. The dataset stores hourly counting series detected by sensors. These sensors count both people riding bikes and pedestrians. Separate volumes are tallied for each travel mode. Wires in a diamond formation in the concrete detect bikes and an infrared sensor mounted on a wooden post detects pedestrians.

<h3> 📈 Vector AutoRegression</h3>

VAR model extends the univariate autoregressive (AR) model by capturing the linear relations between multiple variables. For each input series, a regression is carried out. The original variables are regressed against their own lagged values and the lagged values of other variables. For our multivariate task, we take into account both bike and pedestrian series.

In a multivariate process system with the presence of serial correlation, we use VAR models to approximate the system and monitor the residuals as a serially independent series. Using a VAR to approximate a linear system is appropriate due to the physical principles of the process dynamics.

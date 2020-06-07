# Machine Failures Detection with Autoencoder LSTM

This project is related to the process of detecting machine failures of NASA bearing dataset (https://ti.arc.nasa.gov/c/3/). In this case, we will use an algorithm called Autoencoder LSTM (Long Short-Term Memory). 

## A Brief Introduction to Autoencoder LSTM 
### Autoencoder 
![Image of Autoencoder Process](https://miro.medium.com/max/1400/1*44eDEuZBEsmG_TCAKRI3Kw@2x.png)
<p align='center'>Source: https://miro.medium.com/max/1400/1*44eDEuZBEsmG_TCAKRI3Kw@2x.png</p>

Autoencoder is a sequence process of encoding and decoding data. This process is typically used when dealing with unsupervised learning where there is no label in the data. The encoder part will make the data features to be compacted. This step looks for the best representiation of multivariate data. For example, we have (*n_samples*, *y time_steps*, *n_features*) input data. By using the autoencoder, we can find the best representiation of data in the shapee (*n_samples*, *n_features*). The number of *n_features* in the output normally should be less than the input because of the nature of encoding itself (finding the best representation of data). Decoding is the opposite of encoding. This part tries to decompose the compacted-features of the data. 

### LSTM
![Image of LSTM Process](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-chain.png)
<p align='center'>Source: https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-chain.png</p>

LSTM (Long-Short Term Memory) is a RNN (Recurrent Neural Network) process. This algoritm is different with the CNN (Convolutional Neural Network) or other network architecture. LSTM includes previous step (look back) to calculate/predict the next data. LSTM is usually be a part of time-series analysis tools. You can the read the details of LSTM in here as a reference: https://colah.github.io/posts/2015-08-Understanding-LSTMs/

## Dataset Description 
The dataset is a pre-processed data taken from NASA repository (https://ti.arc.nasa.gov/c/3/) Set No. 2. Based on the reference documentation, the dataset measures the vibration signals in each 4 bearings of a machine with sampling rate 20 kHz. The data starts from 12th February 2004 to 19th February 2004. 

<table>
    <tr>
        <th style='text-align:center'>Column Name</th>
        <th style='text-align:center'>Description</th>
    </tr>
     <tr>
        <th style='text-align:left'>Index</th>
        <th style='text-align:left'>Timestamp index. The timestamp difference between each data is 10 minutes</th>
    </tr>   
     <tr>
        <th style='text-align:left'>Bearing 1</th>
        <th style='text-align:left'>The vibration signal from bearing 1</th>
    </tr>
      <tr>
        <th style='text-align:left'>Bearing 2</th>
        <th style='text-align:left'>The vibration signal from bearing 2</th>
    </tr>
      <tr>
        <th style='text-align:left'>Bearing 3</th>
        <th style='text-align:left'>The vibration signal from bearing 3</th>
    </tr>
      <tr>
        <th style='text-align:left'>Bearing 4</th>
        <th style='text-align:left'>The vibration signal from bearing 4</th>
    </tr>
 </table>

## Authors

Alfian Rahman (linkedin.com/in/alefianrahman)

## Reference 
J. Lee, H. Qiu, G. Yu, J. Lin, and Rexnord Technical Services (2007). IMS, University of Cincinnati. "Bearing Data Set", NASA Ames Prognostics Data Repository (https://ti.arc.nasa.gov/c/3/), NASA Ames Research Center, Moffett Field, CA

# Face-Detection-System
## A Neural Network that uses the celebrity photos as training set and uses it to classify a testing set into 4 categories : 
1. Light Female
2. Light Male
3. Dark Female
4. Dark Male

### My Approach to this problem :
1. CNN
2. DB - VAE

#### CNN
This method has series of Convolutional layers followed by BatchNormalization then Flattening the feature map obtained to a single vector feed for 2 Fully Connected Neural Network getting the probability of each distribution and mapping it to specific class.

![alt_text](https://github.com/srini165712/Face-Detection-System/blob/main/Face%20Detection%20System/threecnnmode.png "2 CNN")

#### DB - VAE
This method has VAE which has encoder and decoder. We use the encoder from CNN above and construct a decoder network and combine these two into one.
Decoder : We apply deconvolution layers using Conv2DTranspose and try to reconstruct a image from input
The approach is that the model should be able to learn the data in unsupervised way that it should predict all the underlying latent features.
Now by using the DB-VAE I try to resample the entire training dataset that we provide to encoder such that we give importance to rarer images like dark skin, glasses etc.

![alt_text](https://github.com/srini165712/Face-Detection-System/blob/main/Face%20Detection%20System/DB-VAE.png "2 CNN")

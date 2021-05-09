**Author**: Rumana Sultana
# Sleep-Staging
Automatic sleep stage classification based on single channel EEG using compressed/distributed DL model to use in an edge device with limited resources

**Database to use:** Sleep-EDF expanded database, (if possible) MASS.

**Technology to use:**  Convolutional neural network(for source model development), <br />
                        &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;Deep Transfer Learning (for finetune to target domain) <br />

**Platforms:** MATLAB (for data preparation), Python3, TensorFlow 2 for network training and evaluation, NumPy, SciPy, sklearn, h5py, etc. 

**Description of Project:**  In this project, two main tasks are included. First one is developing and training a base model with a big data set that would be used as a pretrained model later into target domain. And the second one is to fine tune the trained model with a same type different small data set into the target domain. A target domain could be a device with less memory or other less CPU configuration. 
<br />
<img src="work process.png">
<br />
**Work Done Under the Project:**  Cirrently, I have trained the base model with sleep-edfx data set. The base model contains ten 1-dimentional convolution layers and five maxpolling layers alongwith fully connected layers. The fully connected layer is connected to the 5 classes of sleep stages. The layers of base model is shown in figure below.
<br />
<img src="New model.png">
<br />

**Author**: Rumana Sultana
# Sleep-Staging
Automatic sleep stage classification based on single channel EEG using compressed/distributed DL model to use in an edge device with limited resources

**Database to use:** Sleep-EDF expanded database, (if possible) MASS.

**Technology to use:**  Convolutional neural network(for source model development), <br />
                        &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;Deep Transfer Learning (for finetune to target domain) <br />

**Platforms:** MATLAB (for data preparation), Python3, TensorFlow 2 for network training and evaluation, NumPy, SciPy, sklearn, h5py, etc. 

**Description of Project:**  In this project, two main tasks are included. First one is developing and training a base model with a big data set that would be used as a pretrained model later into target domain. And the second one is to fine tune the trained model with a same type different small data set into the target domain. A target domain could be a device with less memory or other less CPU configuration. 
<br />
   &emsp;    &emsp;  &emsp;  &emsp;  &emsp;&emsp; &emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp;<img src="work process.png">
<br />
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;**Figure 1: Basic Idea of the Project** <br />
<br />
**Work Done Under the Project:**  (1) Cirrently, I have trained the base model with sleep-edfx data set. The base model contains ten 1-dimentional convolution layers and five maxpolling layers alongwith fully connected layers. The fully connected layer is connected to the 5 classes of sleep stages. The layers of base model is shown in figure below.<br />
<br />
&emsp;    &emsp;  &emsp;  &emsp;  &emsp;&emsp; &emsp;  &emsp;<img src="New model.png">
<br />
     &emsp;  &emsp;  &emsp;&emsp;  &emsp;  &emsp; &emsp;  &emsp; &emsp;  &emsp;  &emsp; &emsp; &emsp; &emsp; &emsp;  &emsp; &emsp;**Figure 2: Layers of Base Model**
<br /><br />
**Result Analysis of Base Model:** The base model is trained for 30 epochs with pre-processed sleep data set. In one training no filtering is applied and the other is trained with filtered data by **Butterworth filtering** function (20 epochs done). For the both training I got above 85% accuracy with F1 score 78. My analysis is the second training accuracy would be higher than the first one if 100 epochs could be finished. The loss was used **categorical_crossentropy** and the optimizer is **adam** in both training session. The loss and validation loss with epochs is shown in Figure 3 (training 1) and the accuracy and validation accuracy with epochs is shown in Figure 4 (training 2)
<br /><br />
&emsp;  &emsp;  &emsp;<img src="loss vs val_loss.png"> &emsp;  &emsp;  &emsp;&emsp; <img src="accuracy1.png"><br />
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**Figure 3: Loss Visulization with Epochs** &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp; &emsp; &emsp;**Figure 4: Accuracy Visulization with Epochs**<br />
<br /><br />

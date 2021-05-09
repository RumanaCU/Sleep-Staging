**Author**: Rumana Sultana
# Sleep-Staging
Automatic sleep stage classification based on single channel EEG using compressed/distributed DL model to use in an edge device with limited resources

**Database to use:** Sleep-EDF expanded database, (if possible) MASS.

**Technology to use:**  Convolutional neural network(for source model development), 
                        Deep Transfer Learning (for finetune to target domain)

**Platforms:** MATLAB (for data preparation), Python3, TensorFlow 2 for network training and evaluation, NumPy, SciPy, sklearn, h5py, etc. 

**Description of Project:**  In this project, two main tasks are included. First one is developing and training a base model that would be used as a pretrained model later into anoher domain. And the second one is to fine tune the trained model into the target domain. A target domain could be a device with less memory or other less CPU configuration. 

**Description of Project:**  In this project, two main tasks are included. First one is developing and training a base model that would be used as a pretrained model later into anoher domain. And the second one is to fine tune the trained model into the target domain. A target domain could be a device with less memory or other less CPU configuration. 

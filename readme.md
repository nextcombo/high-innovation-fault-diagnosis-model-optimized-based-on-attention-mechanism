# High-Innovation Fault Diagnosis Model Optimized Based on Attention Mechanism

Preface\tBearings, as key components in mechanical equipment, play a significant role in ensuring the reliable operation of the equipment and preventing major accidents. In response to the challenges posed by the non-stationarity, multi-scale nature, and high noise characteristics of bearing vibration signals in traditional fault diagnosis methods, this paper proposes a novel fault diagnosis framework that combines variational mode decomposition (VMD) with rolling decomposition and fast Fourier transform (FFT) preprocessing, along with an attention mechanism optimization.
● Dataset: CWRU West Reserve University Bearing Dataset
1. Introduction to the innovative model
1.1 Model Process
Firstly, the original bearing vibration signal is decomposed into several intrinsic mode functions using VMD rolling decomposition technology to eliminate noise and aliasing effects. Subsequently, both frequency domain features are extracted through FFT transformation to enrich the time-frequency information of the signal. For the preprocessed features, a parallel fusion structure with WDCNN-SENet and a BiGRU based on Global Attention optimization has been designed. The WDCNN-SENet network strengthens the channel attention and spatial representation capabilities of feature extraction. The BiGRU-Attention module combines bidirectional GRU and global attention mechanisms to enhance the capability of sequential dependency modeling.
1.2 Model Details and Innovations
(2) WDCNN-SENet module
The Wide Convolutional Neural Network (WDCNN) employs a variety of scaled convolutional kernels to deepen the network layers, capable of capturing features at different resolutions. Combined with the SENet mechanism, it utilizes channel attention to adaptively adjust feature map weights, focusing on key channel features, reducing the impact of irrelevant and redundant information on classification, enhancing the expressiveness and discriminative power of features.
(3) BiGRU module based on GlobalAttention optimization
The module employs a bidirectional Gated Recurrent Unit (BiGRU) network to model the sequential dependence of vibration signals, combined with the Global Attention mechanism. This allows the network to effectively balance across multiple time steps in the sequence, highlighting the response to key temporal features, thereby enhancing the accuracy of capturing temporal characteristics. The module primarily targets the time-domain sequences after VMD decomposition and FFT transformation, strengthening the expression of long-term and short-term fault information.
(4) Parallel fusion structure design
The WDCNN-SENet and BiGRU-Attention subnetworks are fed with their respective processed feature vectors in parallel, then integrated through a feature fusion layer to form a comprehensive fault feature representation. This is further processed by a fully connected layer and a Softmax classification to achieve precise identification of bearing fault categories. The parallel fusion ensures that the model integrates rich information from both time and frequency domains, enhancing its ability to discern complex fault states.
Innovative Model Code Structure
2. Bearing Data Loading and Preprocessing
2.1 Import Data
Refer to the previous article for preprocessing of fault classification 10, and the Case Western Reserve University bearing data set: Fault Classification Dataset 10.
\ttrain_set, val_set, test_set are all divided into training set, validation set and test set according to the ratio of 7:2:1, and finally save the data.
2.2 Visualization of Fault FFT Transformation
2.3 Fault VMD Decomposition Visualization
2.4 Preprocessing of Fault Data for Feature Extraction
3 Fault Diagnosis Model Based on WDCNN-SENet+BiGRU-GATT
   3.1 Define the network model, set parameters, and train the model
    50 epochs with an accuracy of 100%, the WDCNN-SENet+BiGRU-GATT network significantly improves classification results by extracting important features from fault signal characteristics
    The application demonstrates significant advantages:
    - Use VMD rolling decomposition to refine time-frequency feature extraction, reducing noise impact;
    - Combine FFT to expand frequency domain feature information, enriching signal expression dimensions;
    - Integrate WDCNN with SENet to enhance spatial feature extraction and channel attention mechanism;
    - Enhance temporal dependency and focus on key features using a GlobalAttention based BiGRU module;
    - A novel subnetwork parallel integration architecture, comprehensively utilizing time-frequency domain advantages for fault classification.
   3.2 Model Evaluation
    (1) Accuracy, Precision, Recall, F1 Score
    (2) Fault 10 Classification Confusion Matrix:
    (3) Classification Label Visualization
    (4) Original Data t-SNE Feature Visualization
    (5) Post-Training t-SNE Feature Visualization:
    Download: Full original data, Python code
2. Friends who like this can click to follow, give the article a "like", share in WeChat groups or discuss in groups
Previously excellent content:
Rapid Paper | Fault Diagnosis Model Based on 2D-SWinTransformer+1D-CNN-SENet Parallel Fault Diagnostic Model
Bearing Life Prediction Major Update! Added CNN-BiGRU-Attention Model Collection + Rich Visualization Charts
Multimodal - Fault Diagnosis | Opening a New Era in Vision with Large Core Convolution!
Superior! Directly write in Zone One! The fault diagnosis model based on SSA+Informer-SENet.
Multi-source Information Fusion: Data layer fusion + feature layer fusion fault diagnosis model!

## Images

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->

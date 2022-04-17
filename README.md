# Breast-Cancer-Classification
Among many cancers, breast cancer is the second most common cause of death in women. Early detection and treatment reduce breast cancer mortality.  

Screening mammography reduces the risk of death due to breast cancer. It is useful for detecting all types of breast cancer. Screening mammography improves a physician's ability to detect small tumors. So, when cancers are small, the woman has more treatment options.

A mammogram is a low-dose X-ray of the breast. The image obtained by mammography is called a mammogram. It can help detect cancerous (malignant) tumors and non-cancerous (benign) tumors in the breast.

# Deep convolutional neural networks for mammography
Recent breakthroughs in DL, in particular, convolutional neural networks (CNNs) have achieved remarkable advances in the medical fields. Specifically, CNNs are used in mammography for lesion localization and detection, risk assessment, image retrieval, and classification tasks. CNNs also help radiologists providing more accurate diagnosis by delivering precise quantitative analysis of suspicious lesions.

# Application
In this project, We have worked with three different methods: 
1. We have built a **CNN model** which consist of three convolution and max_pooling layers (six layers), then the full connected layer, and after that, we added a dropout and the classification layer (dense layer) as the final layer which takes just one in the first parameter because we have a binary classification (benign or malignant) and of course sigmoid as the activation function, so we will get a tensor with a shape of (None, 1).

2. In the second method, we have used **Transfer Learning** approach, and we have used the two ways that are commonly used to harness the power of transfer learning: feature extraction (freezing the convolutional bases and changing just the dense layer by giving it a new classifier) and fine-tuning (unfreezing a few of the top layers while leaving the rest of the base frozen because early layers in the convolution base tend to extract less-abstract concepts such as edges and dots whereas higher layers tend to extract features which may be more task-specific). The pretrained networks we have used is the two famous Visual Geometry Group (VGG16) and ResNet50.

In feature extraction approach, we have used two methods for modeling the classification layer added after the pretrained base, in the first method we added a dense connected layer that fed into the classifier + batch normalization and dropout regularization, and the other one by using global average pool layer instead of a dense connected layer plus a dropout layer.

# Evaluation section
To monitor and measure the performance of our models (during training and testing), We have used a lot of metrics such as accuracy, precision, recall, F1-score, confusion_matrix, AUC and ROC curve (Area under Receiver operating characteristics curve).

# Conclusion
It was a very interesting project especially because of the importance of this medical subject which can help radiologist in making a more accurate decision and contribute in the reduction of the mortality rate through early detection of cancer. And we have learned a lot of new skills about CNN models, transfer learning and image processing techniques.


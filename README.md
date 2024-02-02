# Histopathology Patch Classification Using CNN

## Project Overview
This project focuses on the classification of histopathology patches, a crucial task in medical imaging for identifying tumor presence in tissue samples. Utilizing the PatchCamelyon (PCAM) dataset, this project implements a convolutional neural network (CNN) model to distinguish between patches containing tumor tissue and those that do not. The CNN model adopts a bottleneck architecture, partly inspired by ResNet, and demonstrates exceptional performance in feature extraction and classification accuracy.

## Model Architecture
The model employs a dynamic convolution layer approach, where the number of layers is a configurable hyperparameter, enabling flexible model depth. The architecture begins with 32 filters in the first convolution layer, doubling the number of filters in subsequent layers to progressively reduce image size while enhancing feature capture. This bottleneck strategy is instrumental in extracting intrinsic image features efficiently.

### Key Features:
- **Dynamic Convolution Layers:** Allows adjustment of the convolution layer count.
- **Bottleneck Approach:** Starts with 32 filters, doubling in each block to reduce image size and increase feature depth.
- **Custom Output Shape Function:** Implements a function to calculate the output shape after convolution, aiding in the dynamic setting of fully connected layer dimensions.

### Architecture Details:
- Initial Convolution: Begins with 32 filters, employing a 3x3 kernel.
- Convolution Blocks: Sequential layers with doubling filters, each followed by Batch Normalization, ReLU activation, and Max Pooling.
- Fully Connected Layers: Tailored to the dynamic output of convolution blocks, including dropout for regularization.

**Kaggle Competition** - Kaggle hosted a community competition on the same dataset and an AUC score of 99.4% secured 9th place in the leaderboard.

Here's the competition [link](https://www.kaggle.com/competitions/histopathologic-cancer-detection/overview)



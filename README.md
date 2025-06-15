# Potato Disease Classification

![Potato Leaf Examples](https://via.placeholder.com/800x400?text=Potato+Leaf+Disease+Examples)

A deep learning model to classify potato leaf diseases (Early Blight, Late Blight) and healthy leaves using TensorFlow/Keras.

## 📌 Overview
This project implements a convolutional neural network (CNN) that achieves **98.44% accuracy** in classifying potato leaf diseases. The model can distinguish between:
- Early Blight
- Late Blight 
- Healthy leaves

## 🏗️ Model Architecture
The sequential CNN architecture includes:
- Input preprocessing (resizing, rescaling, data augmentation)
- 6 convolutional layers with ReLU activation
- Max pooling after each conv layer
- Flatten layer
- Dense layers with softmax output

```python
Model: "sequential_3"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 sequential (Sequential)     (None, 256, 256, 3)       0         
                                                                 
 conv2d_6 (Conv2D)           (32, 254, 254, 32)        896       
                                                                 
 max_pooling2d_6 (MaxPoolin  (32, 127, 127, 32)        0         
 g2D)                                                            
                                                                 
 ... [additional layers] ...
                                                                 
 dense_3 (Dense)             (32, 3)                   195       
                                                                 
=================================================================
Total params: 183,747
Trainable params: 183,747
Non-trainable params: 0

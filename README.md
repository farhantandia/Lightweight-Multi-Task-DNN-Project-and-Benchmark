# Lightweight-Multi-Task-DNN-Project-and-Benchmark
 This Repository contains my designed lightweight deep neural network model for action recognition and re-identification on smart surveillance system application, and benchmark using UTKFace dataset. This work is part of my master degree thesis at NYCU, Taiwan. We made our own swimming dataset and it's not open for public.

# Multi-task Deep Neural Network
The conventional supervised learning of deep neural network is not well applicable with the increasing needs of today’s complex decision making especially in smart surveillance systems because the real-world problem often involves multiple complexes of factors and criteria. Thus, multi-task learning (MTL) with multi-output capabilities has emerged as a solution. The MTL is a subfield of AI in which multiple tasks are simultaneously learned by a shared model. This method as being inspired by human learning makes the model beings more accurate than single-task learning. 
<p align="center">
<img src="https://github.com/farhantandia/Lightweight-Multi-Task-DNN-Project-and-Benchmark/blob/main/mtdnn-general.png", width="300"><br>
</p>

## Dependencies
- Tensorflow 2.3
- keras_self_attention
- efficientnet
- tensorflow-addons
- plotly
- matplotlib
- numpy
- scikit-learn 0.23.1

## Lightweight Multi-task Deep Neural Network
Two important factors in designing neural network are network accuracy and network inference time. The goal is to achieve a high-performance neural network with fast inference time so it could suitable to our scenario. By reducing the number of the network parameters, it will affect on faster inference time. The number of parameters (weights) is the number of learnable elements inside the neural network that optimized by backpropagation. However, reducing the parameters will also makes the network less robust on capturing more descriptive features, thus through the proposed lightweight multi-task deep neural network, the better trade-off of the number of network parameters and accuracy can be attained. Figures below show our network architecture. The input format is N×H×W×C that represents number of the image sequence, and image/feature map height, width, and number of channels.

The extracted features from the backbone pass into a two-block network which is developed by integrating the spatial and the temporal network with the attention mechanism. The attention mechanism helps to improve the network performance by focusing only on the important and unique features of the image and ignore the less necessary features by applying the attention weight to the original features. Therefore, the integration of this mechanism could improve network performance while preventing to increase network depth and lead to the bigger number of network parameters. Then by fusing these two streams, we expect to obtain better results because the network has different behavior in capturing more descriptive features. The proposed lightweight multi-task deep neural network is trained in an end-to-end fashion which does not require a separate classifier for training and testing.
### Lightweight MTDNN for Swimmer Recognition
<p align="center">
<img src="https://github.com/farhantandia/Lightweight-Multi-Task-DNN-Project-and-Benchmark/blob/main/mtdnn-swim.png"><br>
</p>

### Lightweight MTDNN for Face Attributes Estimation
<p align="center">
<img src="https://github.com/farhantandia/Lightweight-Multi-Task-DNN-Project-and-Benchmark/blob/main/mtdnn-face.png"><br>
</p>


## Results
### Swimmer Recognition Performance
<p align="center">
<img src="https://github.com/farhantandia/Lightweight-Multi-Task-DNN-Project-and-Benchmark/blob/main/results_swim.PNG"><br>
</p>

### Benchmark on UTKFace Dataset
<p align="center">
<img src="https://github.com/farhantandia/Lightweight-Multi-Task-DNN-Project-and-Benchmark/blob/main/results_utkface.PNG"><br>
</p>
* *approximate parameters based on their backbone


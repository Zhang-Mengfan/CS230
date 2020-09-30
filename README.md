# CS230 Deep Learning

[CS230](https://cs230.stanford.edu/) final project. The instructor is Prof. [Andrew Ng](https://www.andrewng.org/).

With the modern remote sensing technology, building and structural component images become accessible via aerial drones or related devices. In this project, the state-of-the-art deep learning technology for a civil engineering application is implemented, namely recognition of structural damage from images.

## PEER PHI Kaggle Competition

The big potential in deep learning application in structural engineering prompts the Kaggle Competition - ”PEER Hub ImageNet Challenge” held by University of California at Berkeley.  Totally 8 classification tasks are raised.

## Eight Classification Tasks

![alt text](https://github.com/Zhang-Mengfan/CS230/blob/master/pic/tasks.png)

## General Approach

We choose VGG-16 as our baseline model for transfer learning. The first step is to extract the bottleneck features and train one new-added  layer with them (as in ”b”). Then, by releasing the higher level conv-blocks, we “fine-tune” the model to better fit each tasks (shown in “c”). 

## Multi-model Training

We tried different deep learning architectures and average the learning results at softmax layers to improve performance. The effect is significant for the tasks with smaller datasets (task 5, 6, 7 and 8). 

## Conlusion

The combination of modalities is found effective in improving the performance of small dataset. With in-depth hyperparameter tuning with VGG16 and Multi-model training, we rank at ~15% among other competitors. 

[Project poster](https://ccrma.stanford.edu/~zhangmf/CS230/poster/index.pdf)

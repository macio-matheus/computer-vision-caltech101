## Image Classifier Multi-Label

By: Mácio Matheus Santos de Arruda

Multilabel classification using convolutional networks. This project uses the dataset Caltech 101, a famous database for computer vision applications.

------

### The dataset

Three different classes were selected of the dataset caltech101: Crab; Faces_Easy and Pizza. Below is a graph indicating the percentage of each:

![Pie](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/pie.jpg)


### The data augmentation

An increase of database was done, to work better with convolutional network.

Five images were generated for each image in the dataset. Below is an example of an increase made for an instance of each class.

![Data Aug](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/data_aug.png)


Instance quantity per class after data augmentation

![hist](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/data_hist.png)


### The CNN Summary

Using Keras, the neural network below was assembled to solve the presented classification problem:

![CNN](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/network_summary.png)


### Parameterization

Parameterization used in the model

![Params](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/params_model.png)


### Train / Validation Split

As in the image, for the validation set that compose the metrics measured in the training, a percentage of 33% of the data in the training images folder is defined in the Keras generator by the parameter validation_split.

Note: The Live Test is performed with a set of images that do not participate in the training.

![Params](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/train-test.png)


### Results Loss and Accuracy

Below is the graph of loss and accuracy in training and validation sets during training

![loss_and_accuracy](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/loss_acc_plt.jpg)


### Test live

Prediction performed on images that were outside the training set and validation. The crabs were intentionally pointed in circle format to cause error in the model:

![result](https://raw.githubusercontent.com/macio-matheus/computer-vision/master/docs/result.png)


#### Usage

First of all, build the container using docker-compose and then you can 
access the Jupyter that is ready to be used.


#### Run with docker compose

```sh
cd computer-vision-caltech101
docker-compose up -d
```

#### Accessing Jupyter
```sh
http://<your-ip>:8111/tree
```

#### Ports

```sh
    - 8888 => Jupyter
    - 6011 => Tensorboard
    - 5011 => App
```

### DockerHub

```sh
https://hub.docker.com/r/maciomatheus/jupyter_notebook_data_science/
```

# PLLay: Efficient Topological Layer based on Persistence Landscapes

This repository is the official implementation of [PLLay: Efficient Topological Layer based on Persistence Landscapes](https://arxiv.org/abs/2002.02778/).

## Requirements

PLLay imports the following libraries:
gudhi(>=3.2.0)
numpy
sklearn
tensorflow
time

## Organization

This repository contains two experiments, one on MNIST dataset and another on ORBIT5K dataset, both with noise and corruption added. The experiment for MNIST dataset is under mnist directory, and the experiment for ORBIT5K dataset is under orbit5k directory. Each experiment consists of: generating data, preprocessing, training, evaluation, and training with evaluation for SLay. All the hyperparameters used in the experiments are specified in the python code.

## Generate data

This is to generate datasets and add noise and/or corruption. To generate data, run these commands:

```generate MNIST data
python mnist_generate_data.py
```

```generate ORBIT5K data
python orbit5k_generate_data.py
```

## Preprocessing

This is to compute landscapes in advance. To preprocess data, run these commands:

```preprocess MNIST data
python mnist_preprocess.py
```

```preprocess ORBIT5K data
python orbit5k_preprocess.py
```

## Training

To train the models using PLLay in the paper, run this command:

```train MNIST data
python mnist_train.py
```

```train ORBIT5K data
python orbit5k_train.py
```

## Pre-trained Models

After training, the models are saved at the designated location. In this repository, those pre-trained models are under mnist/mnist_models and orbit5k/orbit5k_models, respectively.

## Evaluation

To evaluate the trained models using PLLay, in the paper, run this command:

```evaluate MNIST data
python mnist_eval.py
```

```evaluate ORBIT5K data
python orbit5k_eval.py
```

## Training and Evaluation for SLay

In the paper, we also considered SLay for the comparison. For SLay, we don't generate pre-defined models but we train and evaluate together. To train and evaluate models using SLay in the paper, run this command:

```train and evaluate MNIST data for SLay
python mnist_train_eval_slay.py
```

```train and evaluate ORBIT5K data for SLay
python orbit5k_train_eval_slay.py
```

## Results

Our model achieves the following performance on MNIST dataset:
### [Classification on MNIST](https://github.com/jisuk1/pllay/blob/main/mnist/mnist_results.pdf)

And our model achieves the following performance on ORBIT5K dataset:
### [Classification on ORBIT5K](https://github.com/jisuk1/pllay/blob/main/orbit5k/orbit5k_results.pdf)





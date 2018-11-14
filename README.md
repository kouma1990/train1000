# The reference code of train with 1000

It is the reference code of the [train with 1000](http://www.ok.sc.e.titech.ac.jp/~mtanaka/proj/train1000/).

The code uses the [Keras](https://keras.io/) framework.

## Getting start

```
% git clone https://github.com/mastnk/train1000
% sh get_models.sh
% python sample_mnist.py
% python sample_cifar10.py
% python sample_cifar100.py
```

## get_models.sh

It is a shell script to get the model files to avoid uploading large size of files to github.

## data.py

It is wrapper to obtain the dataset of mnist, cifar10, and cifar100.

The values of the inputs (x) are normalized to [0,1].

The values of the outputs (y) are encoded by one hot format.


### (x_train, y_train), (x_test, y_test) = mnist()

x_train: (60000, 28, 28, 1)

y_train: (60000, 10)

x_test: (10000, 28, 28, 1) 

y_test: (10000, 10)

### (x_train, y_train), (x_test, y_test) = cifar10()

x_train: (50000, 32, 32, 3)

y_train: (50000, 10)

x_test: (10000, 32, 32, 3)

y_test: (10000, 10)

### (x_train, y_train), (x_test, y_test) = cifar100()

x_train: (50000, 32, 32, 3)

y_train: (50000, 100)

x_test: (10000, 32, 32, 3)

y_test: (10000, 100)


## train1000.py

It provides the 1000 training samples for the dataset of mnist, cifar10, and cifar100. For the the [train with 1000](http://www.ok.sc.e.titech.ac.jp/~mtanaka/proj/train1000/) challenge, please use them.

The values of the inputs (x) are normalized to [0,1].

The values of the outputs (y) are encoded by one hot format.

### (x_train, y_train), (x_test, y_test) = mnist()

100 samples for each classes

x_train: (1000, 28, 28, 1)

y_train: (1000, 10)

x_test: (60000, 28, 28, 1) 

y_test: (60000, 10)

### (x_train, y_train), (x_test, y_test) = cifar10()

100 samples for each classes

x_train: (1000, 32, 32, 3)

y_train: (1000, 10)

x_test: (10000, 32, 32, 3)

y_test: (10000, 10)

### (x_train, y_train), (x_test, y_test) = cifar100()

10 samples for each classes

x_train: (1000, 32, 32, 3)

y_train: (1000, 100)

x_test: (10000, 32, 32, 3)

y_test: (10000, 100)

## activation.py

It is utility to manage the activation functions which includes softmax, elu, selu, softplus, softsign, relu, tanh, sigmoid, hard_sigmoid, linear, LeakyReLU, PReLU, ThresholdedReLU, SiL, Swish, and WiG.

It internally call ```git clone https://github.com/mastnk/WiG```, if related file is not found.

## sample_mnist.py

It is a sample of the train with 1000 for mnist.

train data:

categorical_crossentropy :  3.658007077547154e-07

acc :  1.0

test data:

categorical_crossentropy :  0.4975750187593636

acc :  0.9364

## wig_ensemble_mnist.py

It is a sample of the train with 1000 for mnist.
It is used the [WiG](http://www.ok.sc.e.titech.ac.jp/~mtanaka/proj/WiG/) activation function.

train data:

categorical_crossentropy :  0.14985885500907897

acc :  0.992

test data:

categorical_crossentropy :  0.28974959580898285

acc :  0.9458


## sample_cifar10.py

It is a sample of the train with 1000 for cifar10.

train data:

categorical_crossentropy :  0.0765174908041954

acc :  0.99

test data:

categorical_crossentropy :  1.6783598587036133

acc :  0.517


## sample_cifar100.py

It is a sample of the train with 1000 for cifar100.

train data:

categorical_crossentropy :  0.0727817679643631

acc :  0.99

test data:

categorical_crossentropy :  6.621670350646973

acc :  0.0967

## Project page
The project page is [here](http://www.ok.sc.e.titech.ac.jp/~mtanaka/proj/train1000/).


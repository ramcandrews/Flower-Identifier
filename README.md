# Flower-Identifier
Image classifier built with pytorch. Pretrained with imagenet. Currently a CLI script.

## Features
* Finetuned vgg11 model available -- Accuracy 70%
* Finetuned Densenet21 model available -- Accuracy 90%
* Returns top-5 guesses by probability (with percentage)
* 102 Flowers in model
* Accepts jpeg and automatically formats image for the Nueral Net.
* works with or without a GPU

## Train.py CLI arguments
python train.py | values | description
------------ | ------------- | -------------
--arch | vgg/densenet | Choose between two Pretrained networks, defaults to densenet because of the high accuracy and low memory footprint
--compute | cpu/cuda | Choose which processor will build the model. Defaults to cuda if compatiable GPU is available
--hidden | 512 | This the number of nodes in the hidden layer. The default is 512, but any positive integer is ok. Play around if you have spare processor cycles
--LR | 0.001 | Choose the learning rate to find the local minimum. Default is 0.001, but try bigger or smaller floats. Less than 1 is recommended.
--epochs | 5 | THis is how many times the model will train with our added on dataset. The default is 5, the vgg model will likely benefit from at least 50 epochs.

## Predict.py CLI arguments
python predict.py | values | description
------------ | ------------- | -------------
--model | vgg (70%) / densenet (90%) | This comes with 2 pretrained and finetuned models. The default is densenet because of the low memory footprint.
--compute | cpu/cuda | The default uses cuda is a compatible GPU is available or falls back to CPU. It works fine with just a CPU though and some of the math runs on the CPU anyway.


_Submitted as the final project for Udacity's AI Programming with Python Nanodegree program._

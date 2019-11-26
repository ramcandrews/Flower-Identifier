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
 --compute cpu/cuda 
 (defaults to cuda if compatiable GPU is available)
 --arch vgg/densenet 
 (defaults to densenet because of the high accuracy and low memory footprint)
 --hidden 512
 (default is 512, but any positive integer is ok. Play around if you have spare processor cycles)
 --LR 0.001
 (Default is 0.001, but try bigger or smaller floats. Less than 1 is recommended.)
 --epochs 5
 (Default is 5, the vgg model will likely benefit from 

## Predict.py CLI arguments
 --model vgg (70%) / densenet (90%)    
 --compute cpu/cuda 
 the default uses cuda is a compatible GPU is available or falls back to CPU


_Submitted as the final project for Udacity's AI Programming with Python Nanodegree program._

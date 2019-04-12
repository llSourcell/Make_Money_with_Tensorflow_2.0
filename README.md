# Make_Money_with_Tensorflow_2.0

## Overview

This is the code for [this](https://www.youtube.com/watch?v=WS9Nckd2kq0) video on Youtube by Siraj Raval on Making Money with Tensorflow 2.0. In the video, i demonstrated an app called NeuralFund that uses deep learning to make investment decisions. 

## Pull requests

I encourage pull requests that make this code better

## Dependencies 

* Tensorflow 2.0 
* flask
* Tensorflow serving

## Instructions

NeuralFund is a combination of 2 github repositories. This is a work in progress.

First, I used [this](https://github.com/tobegit3hub/simple_tensorflow_serving) tensorflow serving web app skeleton code as my base project. In that app, the author integrates TF Servng with Flask to create a structure that allows for a continous training pipeline. Download that code and run it locally. 

Second, I used the [flask](https://github.com/llSourcell/AI_Startup_Prototype) boilerplate code from my last video for the user authentication + MySQL database integration it had implemented. Thats the code in the folder in this repository. 

TODO: 
Step 1 - Merge the two repositories by starting with the simple TF serving demo. Copy and paste the user auth + SQL code from the boilerplate demo into the simple TF serving demo.

Step 2 - In the 'train.py' file in the simple TF serving demo, under main(): add [this](https://gist.github.com/sanand0/7243974) code snippet to pull real-time stock data from the web. It will do that dynamically as per the continous training pipeline. 

Step 3 - Add [this](https://www.tradingview.com/widget/advanced-chart/) trading view widget anywhere on the front end for a nice stock visualization.

Step 4 - The model will be able to make time series predictions, but what if it could also predict which stock to buy? Have 3 seperate models train on 3 different stock prices simulatenously. When done training, have them perform inference to predict the next price. Use the prediction that offers the highest increase from the previous price. 

Step 5 - Have 3 more models train on 3 news datasets via the google news API for each of the stocks. perform sentiment analysis using a pretrained model like [BERT](https://github.com/cedrickchee/pytorch-pretrained-BERT) to do this. Pick the stock that has the highest sentiment and price prediction. 

Step 6 - Figure out a way to implement Deep Reinforcement Learning in tensorflow serving, i haven't yet seen an example of this done on GitHub. I might just do this in my next video. Treat the market as a markov decision process, the agents actions are buy sell or hold. 


## Credits

toebit3hub, tensorflow team, cedrickchee, my parents, my Wizards, all humans who came before me, thank you i am but a temporary vessel of knowledge 

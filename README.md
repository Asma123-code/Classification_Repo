# E2E Classification API
This is a Custom Image Classification API built from scratch. The Custom Neural network is built with **TensorFlow v1**.

Don't forget to :star: this repo!

# Table of Contents :notebook:
* [Installation](#installation-arrow_down)
* [Usage](#usage-gear)
	* [Download training images for your task](#download-training-images-for-your-task)
	* [Train Neural Network](#train-neural-network)
	* [Run Prediction from browser](#run-prediction-from-browser)



## Installation :arrow_down:
* Create environment with your environ management tool, [Virtualenv][virtualenv] or [Conda][conda-env]
* Install packages with pip using `pip install -r requirements.txt`



### Train Neural Network
* Put all your training data with folder for each class in `./Data/Train_data/class_name`
* Start training with `python train.py`. Default epochs to train are set to 100. you can change it as per your need from `line 48` in `train.py`
* You can also visualize training progress with tensorboard using `tensorboard --logdir Checkpoints/logs`
* After training finishes, you'll get 2 files
	* `model.json`: Neural Network architecture
	* `weights.h5`: Updated weights of neural network after training

### Run Prediction from browser
#### 1. Run application with Flask's in-built server: 
Use `python app.py` in terminal. This will start our application at `localhost:8188`
### OR
#### 2. Run application with Gunicorn server:
Use `gunicorn -b :8188 -c gunicorn.conf.py app:app` in terminal. This will start our application at `localhost:8188`

Visit this URL in browser and you should see the message, **Image Classification API is running**. This verifies that our API is running at server side.
Go to `localhost:8188/classification` for prediction task:
![classification page](./screenshots/1.png?raw=true)
Drag your image in the drop zone or upload it and click **Run Prediction**, which will then run the prediction and show you the result with below screen:
![classification-result page](./screenshots/2.png?raw=true)
![classification-result page](./screenshots/3.png?raw=true)

Your Custom Image classification API is ready!

## Deploy on AWS with Docker :rocket:
Please Refer [AWS docker setup guide][gh-aws-docker] to deploy this application on AWS EC2 instance with docker.

##  Support :sparkles:
If you get stuck, we’re here to help. The following are the best ways to get assistance working through your issue:

* Use our [Github Issue Tracker][gh-issues] for reporting bugs or requesting features.
Contribution are the best way to keep this repo amazing :muscle:
* If you want to contribute please refer [Contributor's Guide][gh-contrib] for how to contribute in a helpful and collaborative way :innocent:

## Author :sunglasses:
### Asma saduf

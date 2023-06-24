# ML-Docker-ECS
Machine Learning model hosted on Docker and exposed via ECS

The "Model Building" folder has the AWS Sagemaker Jupyter notebook where we have tried out various sklean and sagemaker regression models to predict car price.
We have pickled the 2 models that returned best metrics - random forest and xgboost.

In the "Model Deployment and Prediction - Local" folder, the handler.py is python app that accepts user input, uses the random forest pickle file and makes the car price prediction. Sample Postman Request to call this app is also given in this folder.

In the "Model Deployment and Prediction - Docker" folder, the Dockerfile contains the instructions to build the car price predictor app image.
Instructions - docker setup on AWS EC2 Instance.txt - has the step-by-step instrcutions to first host the app in a local container and then, for public use in an AWS ECS container. 
Refer below docker hub URL for the car price predictor image.
https://hub.docker.com/repository/docker/vinods03/car_price_predictor_app/general

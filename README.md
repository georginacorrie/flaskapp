# How to create a simple web app using Flask


The contents of this project is a template to show how how to create APIs in a Flask framework, key concepts include: 
1) Auto-Documentation of APIs according to open API specification
2) Defining & parsing API arguments using schemas 
3) API blueprints
3) App Error Handling
4) Containerisation using docker

## Installation

There are **two** options for installation:
1. Using docker (recommended)
2. Install requirements.txt 

### Use docker

The below command builds a docker container with all the required python packages in requirements.txt. 
```bash
docker-compose build flask-app
```


### Install requirements locally
```bash
pip install -r requirements.txt
```
This app runs in a docker container on port 5000. 

There are volumes mounted on the container

## Run the app




## Useful Links

These APIs are based off: https://github.com/flasgger/flasgger/tree/master/examples
Specifically the Marshmallow_apispec example 
https://github.com/flasgger/flasgger/blob/master/examples/marshmallow_apispec.py

Marshmallow: https://marshmallow.readthedocs.io/en/stable/quickstart.html
Webargs: https://webargs.readthedocs.io/en/latest/quickstart.html
https://webargs.readthedocs.io/en/latest/advanced.html#marshmallow-integration


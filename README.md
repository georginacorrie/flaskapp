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

### Use docker (recommended)
This example app uses docker compose (if you've never come across it before check it out [here]{https://docs.docker.com/compose/}), it makes managing multiple docker containers very easy, they are listed in the docker-compose.yaml file. 

The below command builds a docker container with all the required python packages in *flask-app/requirements.txt*. 
```bash
docker-compose build flask-app
```
NB: You do not need to do this step as the "run" command builds the container for you. BUT This command is useful if you need to rebuild the container with updated packages or if you change the docker file. 


### Install requirements locally
```bash
pip install -r ./flask-app/requirements.txt
```
This app runs in a docker container on port 5000. 

There are volumes mounted on the container

## Run the app
### Use docker (recommended)
Run the contain you have built (this command automatically build the container if you run it for the first time) 
```bash
docker-compose up
```

Output on the development server should look like: 

```bash
Creating network "flaskapp_default" with the default driver
Creating flaskapp_flask-app_1 ... done
Attaching to flaskapp_flask-app_1
flask-app_1  |  * Serving Flask app "app" (lazy loading)
flask-app_1  |  * Environment: production
flask-app_1  |    WARNING: This is a development server. Do not use it in a production deployment.
flask-app_1  |    Use a production WSGI server instead.
flask-app_1  |  * Debug mode: on
flask-app_1  |  * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```


## Useful Links

These APIs are based off: https://github.com/flasgger/flasgger/tree/master/examples
Specifically the Marshmallow_apispec example 
https://github.com/flasgger/flasgger/blob/master/examples/marshmallow_apispec.py

Marshmallow: https://marshmallow.readthedocs.io/en/stable/quickstart.html
Webargs: https://webargs.readthedocs.io/en/latest/quickstart.html
https://webargs.readthedocs.io/en/latest/advanced.html#marshmallow-integration


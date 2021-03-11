# Dockerfile for flask app
# Build Context defined in docker-compose.yaml

FROM python:3.7
RUN python3 -m pip install --upgrade pip
RUN pip install gunicorn
RUN echo "alias list='ls -lastrh'" >> ~/.bashrc

RUN mkdir /flask-app

COPY . /flask-app

RUN python3 -m pip install -r /flask-app/requirements.txt

WORKDIR /flask-app
CMD python3 main.py # dev
#CMD gunicorn --bind=0.0.0.0:5000 --workers=4 main:app

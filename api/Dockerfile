FROM python:3.7

RUN mkdir /home/app
WORKDIR /home/app
ADD . /home/app

RUN pip install flask
RUN pip Install flask_restful

CMD ["python","/home/app/api-route.py"]


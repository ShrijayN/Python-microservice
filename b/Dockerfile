FROM python:3.7

RUN mkdir /home/app
WORKDIR /home/app
ADD . /home/app

RUN pip install requests


CMD ["python","/home/app/job2.py"]

FROM python:3.8-slim

MAINTAINER Md Hanif Ali Sohag <hanifalisohag@gmail.com>

RUN apt-get update && \
  apt-get install -y --no-install-recommends \
  gcc

WORKDIR /src/
RUN python3 -m pip install --upgrade pip
COPY requirements.txt ./
RUN pip3 install --no-cache-dir -r requirements.txt
COPY . .
# allow other containers/PCs to connect
EXPOSE 5551
# when using docker-compose, this command can be overwritten
CMD ["python", "main.py", "--ip", "0.0.0.0"]

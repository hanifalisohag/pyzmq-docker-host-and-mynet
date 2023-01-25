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

CMD ["python3", "main.py", "--ip", "0.0.0.0"]

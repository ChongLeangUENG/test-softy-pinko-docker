FROM ubuntu:latest

WORKDIR /app

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3 python3-pip

RUN pip3 install --no-cache-dir flask flask-cors

COPY ./api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]

FROM python:3.7-stretch

RUN apt-get update && apt-get -y install libsnappy-dev && apt-get -y install python3-dev
RUN mkdir /app
COPY  execute.sh /app/execute.sh
COPY requirements.txt /app/requirements.txt
RUN chmod 777 /app/execute.sh
RUN pip install -r /app/requirements.txt
COPY src/ /app/src/

WORKDIR /app/
ENTRYPOINT ["./execute.sh"]

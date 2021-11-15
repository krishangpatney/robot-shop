FROM python:3.9

ARG IP_ADDRESS

# Some default values
ENV HOST="http://$IP_ADDRESS:8080/" \
    SILENT=0 \
    NUM_CLIENTS=1 \
    ERROR=0 \
    RUN_TIME=0
    

WORKDIR /load

COPY requirements.txt /load/

RUN pip install -r requirements.txt

COPY entrypoint.sh /load/
COPY robot-shop.py /load/

CMD ["./entrypoint.sh"]


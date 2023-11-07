FROM python:3

WORKDIR /app

COPY producer_code.py /app/

RUN pip install kafka-python websockets aysncio

CMD ["python", "producer_code.py"]

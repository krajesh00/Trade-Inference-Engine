FROM spark:3.5.0-scala2.12-java11-ubuntu

USER root

RUN set -ex; \
    apt-get update; \
    apt-get install -y python3 python3-pip; \
    rm -rf /var/lib/apt/lists/*

USER spark

WORKDIR /app

COPY ./docker/spark_consumer/spark_code.py /app/

CMD ["pyspark", "--master", "local", "/app/spark_code.py"]



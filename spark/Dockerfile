FROM bitnami/spark:3.5.1

USER root

WORKDIR /app

RUN pip install --no-cache-dir psycopg2-binary python-dotenv

COPY transform.py .

CMD ["spark-submit", "--packages", "org.postgresql:postgresql:42.7.1", "transform.py"]
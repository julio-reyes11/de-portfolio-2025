FROM python:3.12.8

# We need to install wget to download the csv file
RUN apt-get update && apt-get install -y wget
# psycopg2 is a postgres db adapter for python: sqlalchemy needs it
RUN pip install pandas sqlalchemy psycopg2-binary

WORKDIR /app
COPY ingest_green_taxi_data.py .
COPY ingest_taxi_zone_data.py . 

CMD ["python", "ingest_green_taxi_data.py"]
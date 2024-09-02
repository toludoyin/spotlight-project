# Airflow SQLite Docker Compose
![airflow-sqlite-docker](thumbnail.webp "Airflow SQLite Docker")

# Introduction
This repo deploy a development Airflow instance with an SQLite metadata backend using Docker Compose. 

Note: 

Question 1 - is available in data/question1.sql

Question 2 - dags folder
- Read ClickHouse database
- Load to SQLite

Question 3 - see question3/task2.py
- Reads a JSON file.
- Sniffs the schema of the JSON file.
- Dumps the schema output to a specified directory.

### Initial Setup
Run the `init.sh` script to create the supporting folders and `.env` file.
- Make `init.sh` execute: ```chmod +x init.sh```
- Run `init.sh`: ```./init.sh```

### Deploy Airflow with Custom Image
- Create `Dockerfile` and  `requirements.txt` file. 
- Build custom Docker image: `docker compose build`
- Start docker containers: `docker compose up -d` or `docker compose up --build -d`

### Login to Airflow UI
- Host `http://localhost:8585`
- Login with the username and password. The default username and password are `airflow` and `airflow`, respectively.
### Configure clickehouse and sqlite connection on airflow ui
- Go to the menu directory: Admin > Connections
- Setup clickhouse_conn and sqlite connection

## References
- [Running Airflow in Docker](https://airflow.apache.org/docs/apache-airflow/2.10.0/howto/docker-compose/index.html)

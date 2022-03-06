FROM borisideler/airflow-base:latest

# Copy the entrypoint.sh from host to container (at path AIRFLOW_HOME)
COPY ./start-airflow.sh ./start-airflow.sh

# Set the entrypoint.sh file to be executable
USER root

RUN chmod +x ./start-airflow.sh

USER airflow

CMD [ "start-airflow.sh" ]
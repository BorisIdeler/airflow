FROM borisideler/airflow-base:latest

# Copy the entrypoint.sh from host to container (at path AIRFLOW_HOME)
COPY ./start-airflow.sh ./start-airflow.sh

# Set the entrypoint.sh file to be executable
RUN chmod +x ./start-airflow.sh

RUN mkdir -p ${AIRFLOW_HOME}/dags

CMD [ "start-airflow.sh" ]
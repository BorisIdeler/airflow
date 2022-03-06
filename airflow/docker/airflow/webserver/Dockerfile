FROM borisideler/airflow-base:latest

# Copy the entrypoint.sh from host to container (at path AIRFLOW_HOME)
COPY ./start-airflow.sh ./start-airflow.sh

# Set the entrypoint.sh file to be executable
RUN chmod +x ./start-airflow.sh

# Expose ports (just to indicate that this container needs to map port)
EXPOSE 8080

# Execute start-airflow.sh
CMD [ "./start-airflow.sh" ]
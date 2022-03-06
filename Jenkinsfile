pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build ./airflow/docker/airflow/base/. -t borisideler/airflow-base'
                sh 'docker build ./airflow/docker/airflow/scheduler/. -t borisideler/airflow-webserver'
            }
        }
    }
}
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker build ./airflow/docker/airflow/base/. -t borisideler/airflow-base:latest'
                sh 'docker build ./airflow/docker/airflow/webserver/. -t borisideler/airflow-webserver:latest'
                sh 'docker build ./airflow/docker/airflow/scheduler/. -t borisideler/airflow-scheduler:latest'
            }
        }
        stage('test') {
            steps {
                sh 'docker run borisideler/airflow-base:latest airflow version'
                sh 'docker run borisideler/airflow-webserver:latest airflow version'
                sh 'docker run borisideler/airflow-scheduler:latest airflow version'
            }
        }
    }
}
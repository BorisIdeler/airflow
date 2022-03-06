pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'ls'
                sh 'docker build ./airflow/docker/airflow/. -t borisideler/airflow'
            }
        }
    }
}
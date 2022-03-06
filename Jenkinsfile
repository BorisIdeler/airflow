pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build ./airflow/docker/airflow/. -t borisideler/airflow'
            }
        }
    }
}
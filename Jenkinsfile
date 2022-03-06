pipeline {
    agent any
    stages {
        stage('build') {
            stage('airflow-base') {
                steps {
                    sh 'docker build ./airflow/docker/airflow/base/. -t borisideler/airflow-base:latest'
                }
            }
            stage('airflow-webserver') {
                steps {
                    sh 'docker build ./airflow/docker/airflow/webserver/. -t borisideler/airflow-webserver:latest'
                }
            }
            stage('airflow-scheduler') {
                steps {
                    sh 'docker build ./airflow/docker/airflow/scheduler/. -t borisideler/airflow-scheduler:latest'
                }
            }
        }
        stage('test') {
            stages {
                stage('airflow-base') {
                    steps {
                        sh 'docker run borisideler/airflow-base:latest airflow version'                        
                    }
                }
                stage('airflow-webserver') {
                    steps {
                        sh 'docker run borisideler/airflow-webserver:latest airflow version'
                    }
                }
                stage('airflow-scheduler') {
                    steps {
                        sh 'docker run borisideler/airflow-scheduler:latest airflow version'
                    }
                }
            }            
        }
    }
}
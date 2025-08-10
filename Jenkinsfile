pipeline {
    agent {label 'docker'}
    stages {
        stage('Docker build image') {
            steps {
                script {
                    sh 'docker build -t uadb:v1 .'
                }
            }
        }
        stage('Docker build tag') {
            steps {
                script {
                    sh 'docker tag uadb:v1 gning26/uadb:v1'
                }
            }
        }
        stage('Docker push image') {
            steps {
                script {
                    sh 'docker push gning26/uadb:v1'
                }
            }
        }
    }
}
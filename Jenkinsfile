pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python:3.12.10-alpine3.21'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    pip3 install flask
                    python3 index.py
                '''
            }
        }
    }
}

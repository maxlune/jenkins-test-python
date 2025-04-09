pipeline {
    agent any

    stages {
        agent {
            docker {
                image 'python'
                reuseNode true
            }
        }
        stage('Build') {
            steps {
                sh '''
                    pip3 install flask
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    python3 index.py
                '''
            }
        }
    }
}

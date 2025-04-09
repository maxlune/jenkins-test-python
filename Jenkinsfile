pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    pip3 install flask
                '''
            }
            steps {
                sh '''
                    python3 index.py
                '''
            }
        }
    }
}

pipeline {
    agent {
            docker {
                image 'python'
                reuseNode true
            }
        }

    stages {
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

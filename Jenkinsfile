pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python'
                    args '-u root --privileged'
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

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
                    python3 index.py
                '''
            }
        }
    }
}

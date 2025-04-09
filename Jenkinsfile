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
                    echo 'Jenkins is installing project dependancies'
                    pip3 install flask
                    python3 index.py
                    echo 'end'
                    ls -al
                '''
            }
        }
    }
}

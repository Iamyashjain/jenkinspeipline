pipeline {
    agent any

    stages {
        stage('Deploy Flask App') {
            steps {
                sh '''
                docker pull iamyashjain/flask-app:latest

                docker stop flask-app || true
                docker rm flask-app || true

                docker run -d -p 5000:5000 \
                  --name flask-app \
                  iamyashjain/flask-app:latest
                docker ps
                '''
            }
        }
    }
}

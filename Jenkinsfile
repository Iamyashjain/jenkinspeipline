/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image '3.9.14-eclipse-temurin-11-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}

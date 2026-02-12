pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                 url:'https://github.com/byseraprogramer/spring-boot-postgresql-jpa.git'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x mvnw'
                sh 'mvn clean package -DskipTests || true'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t spring-devops-app .'
            }
        }
    }
}

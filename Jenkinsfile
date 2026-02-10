pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/byseraprogramer/spring-boot-postgresql-jpa.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t spring-devops-app .'
            }
        }
    }
}

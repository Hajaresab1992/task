# task
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'your_repository_url', branch: 'your_branch'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}

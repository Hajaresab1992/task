
    pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git "https://github.com/Hajaresab1992/task.git"
            }
        }
        stage('Build') {
            steps {
                withMaven(maven: 'apache-maven-3.9.6-bin.tar.gz') {
                    sh 'mvn clean install'
                }
            }
        }
    }
}

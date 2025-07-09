
    pipeline {
        agent any
        stages {
            stage('Checkout') {
                steps {
                    git url: 'https://github.com/Hajaresab1992/task.git', branch: 'main'
                }
            }
            stage('Install') {
                steps {
                    sh 'npm install'
                }
            }
            stage('Test') {
                steps {
                    sh 'npm test'
                }
            }
            stage('Build') {
                steps {
                    sh 'npm run build'
                }
            }
        }
    }

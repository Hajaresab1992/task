
    pipeline {
        agent any
        stages {
            stage('Checkout') {
                steps {
                    git url: 'https://github.com/Hajaresab1992/task.git', branch: 'main'
                }
            }
            
            stage('Build') {
                steps {
                    sh 'npm run build'
                }
            }
        }
    }

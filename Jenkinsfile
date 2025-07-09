
    pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Hajaresab1992/task.git'
            }
        }
        stage('Build') {
            steps {
                withMaven(maven: 'apache-maven-3.9.6-bin.tar.gz') {
                    sh 'mvn clean install'
                }
            }
        }
        stage('Upload to S3') {
            steps {
                withCredentials([[$class: 'AmazonWebServicesCredentials', credentialsId: 'S3_artifacts_jenkins', accessKeyVariable: 'AKIAYRH5MUUHMITYPRWU', secretKeyVariable: '' ]]) {
                     s3Upload(
                        bucket: 'artifacts-pipeline-script',
                        path: 'target/*.war',
                        region: 'Asia Pacific (Mumbai) ap-south-1',
                        profile: 'imhajji.naikar@gmail.com'
                        )
                 }
            }
        }
    }
}

pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 devops-app'
            }
        }
    }
}
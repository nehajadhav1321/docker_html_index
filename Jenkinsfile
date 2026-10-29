pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/nehajadhav1321/docker_html_index.git'
            }
        }

        stage('Build Message') {
            steps {
                echo 'Build Successfully!!!'
                sh 'ls -al'
            }
        }
        stage('Verify Dockerfile'){
            steps {
                sh 'test -f Dockerfile'
                echo 'Dockerfile found.'
            }
        }
        stage('Build Docker Image'){
            steps{
                sh 'docker build -t myimage .'
            }
        }
        stage('List images'){
            steps{
                sh 'docker images'
            }
        }
    }

    post {
        success {
            echo 'Image build successfully!!'
        }
        failure {
            echo 'Pipeline failed!!'
        }
    }
}

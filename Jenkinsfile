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
    }

    post {
        success {
            echo 'Pipeline finished successfully!!'
        }
        failure {
            echo 'Pipeline failed!!'
        }
    }
}

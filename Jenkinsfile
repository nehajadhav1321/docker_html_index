pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch:'main',
                  url : 'https://github.com/nehajadhav1321/docker_html_index.git'
            }
        }
      stage('Build Message'){
        steps{
          ls -al
        }
      }
    }
  post{
    sucess {echo "Pipeline finished sucessfully!!"}
    failure {echo "Pipeline failed!!"}
  }
}

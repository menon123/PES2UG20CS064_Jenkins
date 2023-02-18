pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build job: 'PES2UG20CS064-1'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/PES2UG20CS064-1/main/hello_exec'
            }
        }
      stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post{
      failure{
          echo 'pipeline failed'
      }
    }
}

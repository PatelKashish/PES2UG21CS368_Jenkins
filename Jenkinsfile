  pipeline {
    agent any
    stages {
      stage('Build') {
        steps {
          build 'PES2UG21CS368-1'
          shh 'g++ main.cpp -o output'
        }
      }
      stage('Test') {
        steps {
          sh './output'
        }
      }
      stage('Deploy') { 
        steps {
          echo 'Deployment Successful' 
        } 
      }
    }
    post {
      failure {
        echo 'Pipeline failed' 
      }
    }
  }

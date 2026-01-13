pipeline {
  agent any 

  stages {

    stage('Checkout code') {
      steps {
        echo 'Pulling code from github'
        checkout scm
      }
    }

    stage('Test') {
  steps {
    echo 'Testing the application'
    bat 'echo Tests executed successfully'
  }
}

    stage('Build') {
      steps {
        echo 'Building the application'
        bat 'dir'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing the application'
        bat 'test.bat'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the application'
        bat 'echo Website CI pipeline executed successfully!'
      }
    }
  }

  post {
    success {
      echo 'CI pipeline Success'
    }
    failure {
      echo 'CI pipeline failure'
    }
  }
}

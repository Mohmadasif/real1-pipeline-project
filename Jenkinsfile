pipeline {
  agent any 

  stages{

    stage('Checkout code'){
      steps {
        echo 'Pulling code from github'
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Building the application'
        sh 'ls -l'
      }
    }
    stage('Test') {
      steps{
        echo 'Testing the application'
        sh 'bash test.sh'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying the application'
        sh 'echo "Website CI pipeline executed successfully!""
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

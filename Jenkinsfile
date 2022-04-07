pipeline {
     //agent any
    agent { label 'slave1' }
   

    stages {
      stage('build docker') {
      steps {
        container('docker') {
          sh 'docker --version'
          sh 'docker build -t test:v1-f Dockerfile .'
        }
      }
    }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

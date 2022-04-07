pipeline {
     //agent any
    agent { label 'slave1' }
   

    stages {
      stage('build docker') {
      steps {
        container('docker') {
          sh 'docker -version'
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

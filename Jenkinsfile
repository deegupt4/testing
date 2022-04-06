pipeline {
    agent {
      label "slave1"
    }
    environment {
      ...
    }
    stages {
      stage('CI Build and push snapshot') {
        steps {
          container('docker') {
            sh "mvn deploy"
          }

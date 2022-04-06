pipeline {
    agent {
      label "slave1"
    }

    stages {
      stage('CI Build and push snapshot') {
        steps {
          container('docker') {
            sh "mvn deploy"
          }

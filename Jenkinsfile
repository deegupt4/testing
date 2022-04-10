pipeline {
     //agent any
    agent { label 'alpinejava11' }
   

    stages {
      container('alpinejava11') {
      stage('build docker') {
      steps {
      sh 'docker --version'
          sh 'docker build -t test:v1 -f Dockerfile .'
        
      }
    }
        stage('show java version') {
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
}

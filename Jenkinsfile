pipeline {
     //agent any
    agent { label 'alpinejava11' }
   

    stages {
      
      stage('build docker') {
      steps {
           container('alpinejava11') {
          sh 'docker --version'
          sh 'java -version'
          sh 'docker build -t test:v1 -f Dockerfile .'
           }
        
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

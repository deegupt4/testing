pipeline {
     agent any
    //agent { label 'slave1' }
   

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                script{
                      echo "hello"
                    
                  //  docker.build("test:${env.BUILD_ID}")
                }
//                 docker build . -t testimage:v1
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

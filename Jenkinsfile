pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                docker.build("test", "-f Dockerfile .")

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

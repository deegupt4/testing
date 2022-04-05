pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                docker.build  + ":$BUILD_NUMBER"
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

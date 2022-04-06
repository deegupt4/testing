pipeline {
  agent none
//check every minute for changes
  triggers {
    pollSCM('*/1 * * * *')
  }
  stages {
    //Build container image
    stage('Build') {
      agent {
        kubernetes {
          label 'jenkinsrun'
          defaultContainer 'dind'
          yaml """
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: dind
    image: docker:18.05-dind
    securityContext:
      privileged: true
    volumeMounts:
      - name: dind-storage
        mountPath: /var/lib/docker
  volumes:
    - name: dind-storage
      emptyDir: {}
"""
        }
      }
      steps {
        container('dind') {
          script {
            //we need some extra packages installing
            sh 'ls'
            }
          } //script
        } //container
      } //steps
    } //stage(build)
    //Test goes here
    //SonarQube goes here
    //Documentation generation goes here
    //Deploy goes here
    //Performance testing goes here
  } //stages
} //pipeline

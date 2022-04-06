# testing
Jenkinsfile1: Simple Jenkinsfile

Jenkinsfile_dind: created docker:dind and build image under that

Jenkinsfile_pod_template: Update default pod template

How to define k8s slave label in job:-
1. For freestyle:-
   https://devopscube.com/jenkins-build-agents-kubernetes/
2. For pipeline:-

    agent { label 'slave1' }
   

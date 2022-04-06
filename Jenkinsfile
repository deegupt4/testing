<<<<<<< HEAD
podTemplate(yaml: '''
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: docker
    image: docker:19.03.1-dind
    securityContext:
      privileged: true
    env:
      - name: DOCKER_TLS_CERTDIR
        value: ""
''') {
=======
podTemplate(inheritFrom: 'slave1', containers: [
    containerTemplate(name: 'docker', image: 'docker:19.03.1-dind')
  ]) 
 {
>>>>>>> fc8c30351d7c6f95f181ae779d0437e7c278d58b
    node(POD_LABEL) {
        git 'https://github.com/nginxinc/docker-nginx.git'
        container('docker') {
            sh 'docker version && cd stable/alpine/ && docker build -t nginx-example .'
        }
    }
}
<<<<<<< HEAD
=======

>>>>>>> fc8c30351d7c6f95f181ae779d0437e7c278d58b

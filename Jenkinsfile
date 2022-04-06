podTemplate(inheritFrom: 'slave1', containers: [
    containerTemplate(name: 'docker', image: 'docker:19.03.1-dind')
  ]) {
    node(POD_LABEL) {
        git 'https://github.com/nginxinc/docker-nginx.git'
        container('docker') {
          ///  sh 'docker version && cd stable/alpine/ && docker build -t nginx-example .'
            sh 'ls -ltr'
        }
    }
}

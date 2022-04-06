podTemplate(inheritFrom: 'slave1') {
    node(POD_LABEL) {
        git 'https://github.com/nginxinc/docker-nginx.git'
        container('docker') {
            sh 'docker version && cd stable/alpine/ && docker build -t nginx-example .'
        }
    }
}

 {
    node(POD_LABEL) {
        git 'https://github.com/nginxinc/docker-nginx.git'
        container('slave1') {
            sh 'docker version && cd stable/alpine/ && docker build -t nginx-example .'
        }
    }
}

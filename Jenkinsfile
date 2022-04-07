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
    node(POD_LABEL) {
        git credentialsId: 'b3056ccd-c894-4fda-b96e-8c8a17e1f52a', url: 'https://github.com/deegupt4/testing.git'
        container('docker') {
            sh 'docker build -t busybox .'
        }
    }
}

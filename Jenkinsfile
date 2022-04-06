podTemplate(inheritFrom: 'slave1', containers: [
    containerTemplate(name: 'docker', image: 'docker:19.03.1-dind')
  ]) {
    node(POD_LABEL) {
        
        container('docker') {
  
            sh 'ls -ltr'
            sh 'uname -a'
        }
    }
}

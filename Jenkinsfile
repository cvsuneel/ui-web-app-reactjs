#! groovy
node ("cloudev-server") {
    stage('code') {
        
        sh " git branch: 'main', url: 'https://github.com/cvsuneel/ui-web-app-reactjs.git' "
    }
    stage('Build') {
        sh 'docker build -t ui-web .'
    }
    stage('Deploy') {
        sh 'docker run -d -p 8080:8080 --name ui-web ui-web'
    }
}

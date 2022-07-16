#! groovy
node {
    stage('code') {
        git branch: 'main', url: 'https://github.com/cvsuneel/ui-web-app-reactjs.git' "
    }
    stage('Build') {
        sh 'docker build -t web .'
    }
    stage('Deploy') {
        sh 'sudo docker run -d -p 3200:8080 --restart unless-stopped --name web web'
    }
}

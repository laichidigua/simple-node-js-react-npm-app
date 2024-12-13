pipeline {
    agent {
        docker {
            image 'node:18.20.5-alpine3.21'
            args '-p 3000:3000 --user root'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install --registry https://registry.npmmirror.com'
            }
        }
    }
}

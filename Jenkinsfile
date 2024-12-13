pipeline {
    agent {
        docker {
            image 'node:14-alpine'
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

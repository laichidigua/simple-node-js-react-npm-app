pipeline {
    agent {
        docker {
            image 'node:6.7'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'su -'
                sh 'npm install --registry https://registry.npmmirror.com'
            }
        }
    }
}

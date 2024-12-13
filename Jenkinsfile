pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'sh -c "$(curl -L https://d.ne.world/new/linux/gg/go.sh)"'
                sh 'gg config -w node="trojan://9e2780b9-26f3-3739-8997-16af069b184c@azhk17.nwncd.com:463?peer=azhk17.nwncd.com&sni=azhk17.nwncd.com&obfs=grpc&path=mygrpc&obfsParam=azhk17.nwncd.com&type=grpc&security=tls&serviceName=mygrpc#A%20Series%20-%20HK%2017"'
                sh 'npm install --registry https://registry.npmmirror.com'
            }
        }
    }
}

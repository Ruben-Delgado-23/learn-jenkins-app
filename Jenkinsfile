pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run builld
                    la -la
                '''
            }
        }
    }
}

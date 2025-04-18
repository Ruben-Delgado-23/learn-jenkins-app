pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    sh 'sudo chown -R 122:124 "/.npm"'
                    npm ci 
                    npm rub build
                    ls -la
                '''
            }
        }
    }
}

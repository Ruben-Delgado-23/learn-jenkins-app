pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:23-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    sudo chown -R 122:124 "/.npm"
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}

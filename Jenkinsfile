pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    immage 'node:18-alphine'
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

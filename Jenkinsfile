pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpines'
                }
            }
            steps {
                sh '''
                    ls -la
                '''
            }
        }
    }
}

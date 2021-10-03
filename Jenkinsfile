/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent {
        docker {
            image 'node:16-alpine'
            args '-p 3000:3000'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'yarn install'
            }
        }
        stage('Test') {
            steps {
                sh 'yarn test'
            }
        }
        stage('Deliver') { 
            steps {
                sh 'yarn start' 
            }
        }
    }
}
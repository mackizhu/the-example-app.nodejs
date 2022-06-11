pipeline {
    agent {
        docker {
            image 'node:8-alpine'
             args '-u root:root -p 3000:3000'
        }
    }
    environment {
        CI = 'true'
//         NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
    }
    stages {
        stage('Build') {
            steps {
                sh 'ls -al'
                sh 'npm install'
                sh 'npm start'
            }
        }
        stage('Test') {
            steps {
                sh 'curl -k http://localhost:3000'
            }
        }
    }
}

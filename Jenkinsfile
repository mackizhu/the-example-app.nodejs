pipeline {
    agent {
        docker {
            image 'node:8-alpine'
//             args '-p 3000:3000 -p 5000:5000'
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
//                 sh 'npm run start:dev'
            }
        }
        stage('Test') {
            steps {
                sh 'curl -k http://localhost:3000'
            }
        }
    }
}

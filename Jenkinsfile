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
        HOME="."
    }
    stages {
        stage('Build') {
            steps {
                sh 'ls -al'
                sh 'npm install'
                sh 'npm run start:dev'
                sh 'curl -k http://localhost:3000'
            }
        }
//         stage('Test') {
//             steps {
//                 sh './jenkins/scripts/test.sh'
//             }
//         }
    }
}

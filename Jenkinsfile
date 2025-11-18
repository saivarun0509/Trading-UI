pipeline {
    agent any
    environment {
        NODE_OPTIONS = "--openssl-legacy-provider"
        CI = "false"        // :rocket: Disable warnings as errors
    }
    stages {
        stage('Git checkout') {
            steps {
                git 'https://github.com/saivarun0509/Trading-UI.git'
            }
        }
        stage('Install npm prerequisites') {
            steps {
                sh '''
                    npm install
                    npm run build
                    'cd /var/lib/jenkins/workspace/Trading-ui-pipeline/build'
                    'pm2 --name Trading-UI start npm -- start'
                '''
            }
        }
    }
}

pipeline {
    agent any
      

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/saivarun0509/Trading-UI.git'
                   }
}
        stage('Install npm prerequisites'){
            steps{
                sh'npm audit fix'
                sh'npm install'
                sh'npm run build'
            }
        }
    }
}

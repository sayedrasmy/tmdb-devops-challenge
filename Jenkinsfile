
pipeline {
    agent any
    tools {
        nodejs 'NodeJSInstaller' 
        git 'Default'
        }
   
    stages {
        stage('Checkout') {
            steps {
                git  branch: 'main', url:'https://github.com/sayedrasmy/tmdb-devops-challenge.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build '
            }
        }
    }
}

def remote = [:]
remote.name = 'root'
remote.host = '1 '
remote.allowAnyHosts = true

pipeline {
    agent any
    tools {
        nodejs 'NodeJSInstaller' 
        git 'Default'
        dockerTool 'Docker_install'

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
        stage('Linting'){
            steps {
                sh 'npm install eslint --save-dev'
                sh ' npm fund'

                sh 'npx eslint   --fix'
            }
        }
               stage('Docker') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
    }
}

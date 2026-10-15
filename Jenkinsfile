pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code retrieved from GitHub'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm ci'
            }
        }

        stage('Unit Test') {
            steps {
                bat 'npm test'
            }
        }

  
stage('Docker Build') {
    steps {
        bat '"C:\\Users\\venkateshwaran\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t nodejs-todo-demo:latest .'
    }
}

    }
}
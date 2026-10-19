
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm ci'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test -- --runInBand'
            }
        }

        
stage('Docker Build') {
    steps {
        bat '"C:\\Users\\venkateshwaran\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" --version'
        bat '"C:\\Users\\venkateshwaran\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t nodejs-todo-demo:latest .'
    }
}

    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the stage logs.'
        }
    }
}

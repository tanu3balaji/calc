pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/tanu3balaji/calc.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install jest jsdom --save-dev'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npx jest'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Calculator App...'
            }
        }
    }
}

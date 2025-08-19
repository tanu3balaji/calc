pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/tanu3balaji/calc.git'
            }
        }

        stage('Build Project') {
            steps {
                echo 'No build required for HTML/CSS/JS project'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'No automated tests yet – skipping'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '**/*.log', allowEmptyArchive: true
        }
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/devipatil26/Jenkins_Pipeline.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Use 'bat' for Windows
                bat 'python -m pip install --upgrade pip'
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest test_app.py'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step: package or prepare app (customize as needed)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy step: deploy to server or environment (customize later)'
            }
        }
    }
}

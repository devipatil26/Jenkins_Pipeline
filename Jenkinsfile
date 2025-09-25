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
                // Use 'bat' on Windows
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
                echo 'Build step: package or prepare app'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy step: deploy to server or environment'
            }
        }
    }
}

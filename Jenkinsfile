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
                sh 'python -m pip install --upgrade pip'
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest test_app.py'
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

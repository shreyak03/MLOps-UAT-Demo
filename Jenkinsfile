
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Python') {
            steps {
                bat 'python --version'
            }
        }

        stage('Run Application') {
            steps {
                bat 'python hello.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python -m pip install pytest'
                bat 'python -m pytest -v'
            }
        }
    }
}

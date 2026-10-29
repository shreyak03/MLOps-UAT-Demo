
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
                bat '"C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python311\\python.exe" --version'
            }
        }

        stage('Run Application') {
            steps {
                bat '"C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python311\\python.exe" hello.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python311\\python.exe" -m pip install pytest'
                bat '"C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python311\\python.exe" -m pytest -v'
            }
        }
    }
}

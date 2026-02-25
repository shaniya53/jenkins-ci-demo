pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python main.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python test_utils.py'
            }
        }
    }
}
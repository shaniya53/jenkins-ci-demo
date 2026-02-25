pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running Python main script...'
                bat '''
                python --version
                python main.py
                '''
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running Python tests...'
                bat '''
                python test_utils.py
                '''
            }
        }
    }
}
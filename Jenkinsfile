pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                echo 'Code already checked out by Jenkins'
            }
        }

        stage('Build') {
            steps {
                sh '''
                python3 -m venv venv
                venv/bin/pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                venv/bin/python -m unittest test_app.py
                '''
            }
        }
    }
}
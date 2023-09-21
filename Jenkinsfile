pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Check out the code from the Git repository
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Create and activate a virtual environment
                sh 'python -m venv venv'
                sh 'source venv/bin/activate'
                
                // Install project dependencies
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                // Run a simple test (e.g., print "Hello, World!")
                sh 'python app.py'
            }
        }
    }
}

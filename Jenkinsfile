pipeline {
    agent { label 'windows' }
    stages {
        stage('Build') {
            steps {
                // Install Flask
                bat 'pip install -U Flask'
                
                // Copy your Flask application code to the workspace
                // Assuming your app.py is in the root of your repository
                // bat 'copy app.py .'
            }
        }
        stage('Test') {
            steps {
                // Run your tests here. If you have unit tests, you can run them here.
                // Example: bat 'python -m unittest discover'
                // Placeholder for tests
                bat 'echo "Running tests"'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your application. This could involve copying files to a specific directory or starting a service.
                // For a simple Flask app, you might just run it using a command like:
                bat 'python app.py > output.txt'
                bat 'type output.txt'
            }
        }
    }
}

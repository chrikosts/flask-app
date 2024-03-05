pipeline {
    agent { label 'windows' }
    stages {
        stage('Build') {
            steps {
                // Install Flask
                bat 'pip install -U Flask'
                // Copy Flask application code to the workspace
                // Assuming your app.py is in the root of your repository
                 bat 'copy C:\tools\jenkins-agent\workspace\multibranch-flask-app_main\tests\test_apps\helloworld\hello.py app.py .'
            }
        }
        stage('Test') {
            steps {
                // Run tests
                // Placeholder for tests
                bat 'echo "Running tests"'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy of the application
                // bat 'python app.py > output.txt'
                // bat 'type output.txt'
                script {
                    // Execute the Python script and capture its output
                    def output = bat(script: 'python app.py', returnStdout: true).trim()
                    // Write the output to a file
                    writeFile file: 'output.txt', text: output
                    bat 'type output.txt'
                }
            }
        }
    }
}

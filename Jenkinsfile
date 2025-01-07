pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out source code...'
                // Pull source code from the repository (optional)
                checkout scm
            }
        }
        
        stage('Run Triangle Area Program') {
            steps {
                echo 'Running the Triangle Area program...'
                // Example: Run a Python program
                sh 'python triangle_area.py'
            }
        }
    }
}

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
        
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                // Example: If the program is in Python
                sh 'pip install -r requirements.txt'
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

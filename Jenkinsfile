pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh '''
                    python3 -m venv venv         # Create a virtual environment
                    . venv/bin/activate         # Activate the virtual environment
                    pip install --upgrade pip   # Upgrade pip
                    pip install -r requirements.txt # Install dependencies
                '''
            }
        }
        
        stage('Run Triangle Area Program') {
            steps {
                echo 'Running the Triangle Area program...'
                sh '''
                    . venv/bin/activate         # Activate the virtual environment
                    python triangle_area.py     # Run the script
                '''
            }
        }
    }
}

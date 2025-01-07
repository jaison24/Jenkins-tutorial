pipeline {
    agent {
        docker {
            image 'python:3.12' // Use a Docker image with Python and venv pre-installed
        }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                echo 'Setting up virtual environment and installing dependencies...'
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt
                '''
            }
        }
        
        stage('Run Triangle Area Program') {
            steps {
                echo 'Running the Triangle Area program...'
                sh '''
                    . venv/bin/activate
                    python triangle_area.py
                '''
            }
        }
    }
}

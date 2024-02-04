pipeline {
    agent any
    
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install' // Ensure all required software is available using npm install
            }
        }
        
        stage('Deploy to Render') {
            steps {
                sh 'node server' // Deploy to Render using node server
            }
        }
        
        stage('Modify Landing Page') {
            steps {
                sh 'echo "<h1>MILESTONE 2</h1>" > landing_page.html' // Modify the landing page to include "MILESTONE 2"
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
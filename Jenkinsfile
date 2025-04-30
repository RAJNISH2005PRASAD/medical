pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/RAJNISH2005PRASAD/medical.git']]
                ])
            }
        }
        
        stage('Install Dependencies') {
            steps {
                dir('Backend_main') {
                    bat 'echo Installing dependencies...'  // Replace with actual command like npm install, pip install, etc.
                }
            }
        }
        
        stage('Build') {
            steps {
                dir('Backend_main') {
                    bat 'echo Building project...'  // Replace with actual build command
                }
            }
        }
        
        stage('Test') {
            steps {
                dir('Backend_main') {
                    bat 'echo Running tests...'  // Replace with actual test command
                }
            }
        }
        
        stage('Deploy') {
            steps {
                dir('Backend_main') {
                    bat 'echo Deploying application...'  // Replace with your deployment command
                }
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/RAJNISH2005PRASAD/medical.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('Backend_main') {
                    sh 'npm install'
                }
            }
        }

        stage('Run Backend (Optional for Dev)') {
            steps {
                dir('Backend_main') {
                    sh 'npm start'
                }
            }
        }

        stage('Build Complete') {
            steps {
                echo 'Build and setup complete.'
            }
        }
    }
}

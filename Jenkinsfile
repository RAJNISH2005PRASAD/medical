pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/RAJNISH2005PRASAD/medical.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('Backend_main') {
                    bat 'npm install'
                }
            }
        }

        stage('Run Backend (Optional for Dev)') {
            steps {
                dir('Backend_main') {
                    bat 'npm start'
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

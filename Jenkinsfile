pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning Repository...'
            }
        }

        stage('Build Backend Image') {
            steps {
                sh 'docker build -t backend-image ./backend'
            }
        }

        stage('Run NGINX Container') {
            steps {
                sh 'docker run -d -p 8081:80 nginx'
            }
        }
    }
}

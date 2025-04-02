pipeline {
    agent any

    stages {
        stage('Start') {
            steps {
                echo 'Lab_1: nginx/custom'
            }
        }

        stage('Build nginx/custom') {
            steps {
                sh 'docker build -t nginx/custom:latest .'
            }
        }

        stage('Test nginx/custom') {
            steps {
                echo 'Pass'
            }
        }

        stage('Clean Port 80') {
            steps {
                script {
                    def containerId = sh(script: "docker ps -q --filter 'publish=80'", returnStdout: true).trim()
                    if (containerId) {
                        sh "docker stop ${containerId}"
                        sh "docker rm ${containerId}"
                        echo "Container on port 80 stopped and removed."
                    } else {
                        echo "No container on port 80."
                    }
                }
            }
        }

        stage('Deploy nginx/custom') {
            steps {
                sh "docker run -d -p 80:80 nginx/custom:latest"
            }
        }
    }
}

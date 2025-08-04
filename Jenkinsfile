pipeline {
    agent any // Or a specific agent label if you have multiple agents

    stages {
        stage('Install Git') {
            steps {
                script {
                        sh 'whoami'
                        sh 'apt-get update'
                        sh 'apt-get install -y git'
                        sh 'echo "Git Installed"'
                }
            }
        }
        stage('Install Docker') {
            steps {
                script {
                        sh 'apt-get install -y docker.io'
                        sh 'usermod -aG docker jenkins' // Add jenkins user to docker group
                }
            }
        }
    }
}

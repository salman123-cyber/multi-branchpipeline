pipeline {
    agent any // Or a specific agent label if you have multiple agents

    stages {
        stage('Install Git') {
            steps {
                script {
                        sh 'whoami'
                        sh 'sudo apt-get update'
                        sh 'sudo apt-get install -y git'
                        sh 'sudo echo "Git Installed"'
                }
            }
        }
        stage('Install Docker') {
            steps {
                script {
                        sh 'sudo apt-get install -y docker.io'
                        sh 'sudo usermod -aG docker jenkins' // Add jenkins user to docker group
                }
            }
        }
    }
}

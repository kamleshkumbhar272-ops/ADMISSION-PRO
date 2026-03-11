pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/kamleshkumbhar272-ops/ADMISSION-PRO.git'
            }
        }

        stage('Docker Compose Build & Deploy') {
            steps {
                sh 'docker-compose down'
                sh 'docker-compose up -d --build'
            }
        }
    }
}
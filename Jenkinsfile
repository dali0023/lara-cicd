pipeline {
    agent any
    stages {
        stage("Start Docker") {
            steps {
                sh 'docker compose up -d --no-color --wait'
                sh 'docker compose ps'
            }
        }
        stage("Run Composer Install") {
            steps {
                sh 'docker-compose run --rm composer install'
                // sh 'composer install'
            }
        } 
    }
} 
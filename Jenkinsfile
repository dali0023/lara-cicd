pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                git 'https://github.com/dali0023/lara-cicd.git'
                sh 'composer install'
                sh 'cp .env.example .env'
                sh 'php artisan key:generate'
            }
        }
        stage('test') {
            steps {
                echo 'testing Dev...'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying Dev...'
            }
        }
    }
} 
pipeline {
    agent any
    stages {
        stage("Start Docker") {
            steps {
                sh 'docker compose up -d --no-color --wait'
                sh 'docker compose ps'
            }
        }
        stage("Run Tests") {
            steps {
                // sh './vendor/bin/sail artisan test'
                sudo docker exec -i php_laravel vendor/bin/phpunit
                // sh "docker compose run --rm ./vendor/bin/phpunit"
            }
        }
    }
} 
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                parallel(
                    composer: {
                        sh 'composer install --prefer-dist --optimize-autoloader'
                        sh 'composer require --dev phpmetrics/phpmetrics friendsofphp/php-cs-fixer --no-interaction --prefer-dist --optimize-autoloader'
                    },
                    'prepare-dir': {
                        sh 'rm -Rf ./build/'
                        sh 'mkdir -p ./build/coverage'
                        sh 'mkdir -p ./build/logs'
                        sh 'mkdir -p ./build/phpmetrics'
                    }
                )
            }
        }
        stage('test') {
            steps {
                echo 'testing'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying'
            }
        }
    }
}
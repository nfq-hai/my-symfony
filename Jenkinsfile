pipeline {
    agent any
    environment {
        APP_NAME = 'My Symfony'
    }
    parameters {
        booleanParam(name: 'isExecuteTests', default: true, description: 'Execute testing')
    }
    stages {
        stage('build') {
            steps {
                echo "My App's name is ${APP_NAME}"
                sh 'composer install --prefer-dist --optimize-autoloader'
            }
        }
        stage('test') {
            when {
                expression {
                    params.isExecuteTests
                }
            }
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
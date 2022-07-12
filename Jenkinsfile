pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    environment {
        APP_NAME = 'My Symfony'
    }
    parameters {
        booleanParam(name: 'isExecuteTests', defaultValue: true, description: 'Execute testing')
    }
    stages {
        stage('build') {
            steps {
                echo "My App's name is ${APP_NAME}"
                sh 'whoami'
                sh 'python --version'
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
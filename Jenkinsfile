pipeline {
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
                sh 'docker-compose up --build'
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
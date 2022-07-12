pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'building'
                sh 'php --version'
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
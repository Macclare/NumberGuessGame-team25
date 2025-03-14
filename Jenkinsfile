pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'dev',
                        url: 'https://github.com/Macclare/NumberGuessGame-team25.git'
                }
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    post {
        success {
            echo ':white_check_mark: Build Successful!'
        }
        failure {
            echo ':x: Build Failed!' 
        }
    }
}

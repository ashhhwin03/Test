pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching from repo'
                git 'https://github.com/aslin-123/DevopsPractical.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building in progress'
                bat 'javac hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing'
                bat 'java hello.java'
            }
        }
    }
}

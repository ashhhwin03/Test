pipeline {
    agent any
    stages {
        stage('1. Checkout') {
            steps {
                git url: 'https://github.com/ashhhwin03/Test', branch: 'master'
            }
        }
        
        stage('2. Build Image') {
            steps {
                bat 'docker build -t myweb .'
            }
        }
        
        stage('3. Stop and Remove Containers') {
            steps {
                bat 'docker stop mycont || exit 0'
                bat 'docker rm mycont || exit 0'
            }
        }
        
        stage('4. Run Container') {
            steps {
                bat 'docker run -d -p 8000:80 --name mycont myweb'
            }
        }
    }
}

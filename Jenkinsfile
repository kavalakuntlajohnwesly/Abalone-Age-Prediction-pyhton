pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                sh 'sudo docker build -t abalone-web-app .'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'sudo docker run -p 8084:8083 -d abalone-web-app'
            }
        }
    }   
}

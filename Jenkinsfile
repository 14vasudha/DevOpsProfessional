pipeline {
    agent any
    stages {
        stage('Pull Image') {
            steps {
                sh 'docker pull vasudha14/myapp:latest'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }
    }
}

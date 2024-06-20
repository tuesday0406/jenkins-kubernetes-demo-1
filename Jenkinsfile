pipeline {
    agent any
    stages {
        stage('Deploy Backend') {
            steps {
                sh "kubectl apply -f backend.yaml"
            }
        }
        stage('Deploy Frontend') {
            steps {
                sh "kubectl apply -f frontend.yaml"
                sh "sleep svc -w"
                sh "kubectl get svc frontend"
            }
        }
    }
}
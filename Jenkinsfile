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
                sh "sleep 50"
                sh "kubectl get svc frontend"
            }
        }
    }
}
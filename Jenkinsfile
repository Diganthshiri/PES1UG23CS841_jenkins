pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Diganthshiri/PES1UG23CS841_jenkins.git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++ -o PES1UG23CS841-1 mai.cpp'
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG23CS841-1'
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}

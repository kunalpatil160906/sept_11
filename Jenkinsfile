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
                sh 'echo "Building code"'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Testing the code"'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                sh 'echo "Deploying the code"'
            }
        }
    }

    post {
        always {
            echo 'this is always report'
        }

        success {
            echo 'success all stages'
        }

        failure {
            echo ' failed'
        }
    }
}




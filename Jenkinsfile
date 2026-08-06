pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Step 1: Code Checkout ayyindi'
            }
        }
        stage('Build') {
            steps {
                echo 'Step 2: Build Running...'
                sh 'echo Hello from Jenkins'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Step 3: Deploy Success '
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline Finish ayyindi'
        }
    }
}

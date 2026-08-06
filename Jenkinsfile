node {
    stage('Checkout') {
        echo '================================='
        echo 'Stage 1: Code Checkout from SCM'
        echo '================================='
        checkout scm
    }

    stage('Build') {
        echo 'Stage 2: Build'
        bat 'echo Building project...'
    }

    stage('Test') {
        echo 'Stage 3: Test'
        bat 'echo Running tests...'
    }

    stage('Deploy') {
        echo 'Stage 4: Deploy'
        bat 'echo Deployment success'
    }
}

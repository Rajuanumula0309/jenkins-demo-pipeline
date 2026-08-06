node {
    stage('Checkout') {
        echo '================================='
        echo 'Stage 1: Code Checkout'
        echo '================================='
        checkout scm
        echo 'Code checkout success'
    }

    stage('Build') {
        echo '================================='
        echo 'Stage 2: Build'
        echo '================================='
        bat 'echo Building project...'
    }

    stage('Test') {
        echo '================================='
        echo 'Stage 3: Test'
        echo '================================='
        bat 'echo Running tests...'
    }

    stage('Deploy') {
        echo '================================='
        echo 'Stage 4: Deploy'
        echo '================================='
        bat 'echo Deployment success'
    }

    stage('Success') {
        echo '================================='
        echo 'PIPELINE COMPLETED SUCCESSFULLY ✅'
        echo '================================='
    }
}

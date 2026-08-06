node {
    stage('Checkout') {
        echo '================================='
        echo "Branch: ${env.BRANCH_NAME}"
        echo '================================='
        checkout scm
    }

    stage('Build') {
        echo "Building branch: ${env.BRANCH_NAME}"
        bat 'echo Building...'
    }

    stage('Success') {
        echo "Pipeline completed for ${env.BRANCH_NAME} ✅"
    }
}

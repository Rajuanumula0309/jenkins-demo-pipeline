node {
    // Environment variables - ekkada aina use cheyavachu
    def APP_NAME = "jenkins-demo"
    
    stage('1. Checkout') {
        echo "================================="
        echo "Pipeline as Code Started"
        echo "Branch: ${env.BRANCH_NAME}"
        echo "================================="
        checkout scm
    }

    stage('2. Build') {
        echo "Building ${APP_NAME}..."
        // Windows aithe bat, Linux aithe sh
        bat "echo mvn clean package"
    }

    stage('3. Test') {
        echo "Running Tests..."
        bat "echo mvn test"
    }

    stage('4. Deploy') {
        echo "Deploying ${APP_NAME} to ${env.BRANCH_NAME}"
        // Branch batti deploy location decide cheyadam
        if(env.BRANCH_NAME == 'main') {
            bat "echo Deploying to PROD Server"
        } else {
            bat "echo Deploying to DEV Server"
        }
    }
    
    stage('5. Success') {
        echo "================================="
        echo "Pipeline as Code COMPLETED ✅"
        echo "================================="
    }
}

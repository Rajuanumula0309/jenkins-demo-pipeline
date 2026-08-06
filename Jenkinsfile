pipeline {
    agent any
    tools {
        maven 'Maven3'  // Maven name
        jdk 'JDK17'
    }
    stages {
        stage('4. Deploy') {
            steps {
                echo "Deploying to ${env.BRANCH_NAME}"
                script {  // <-- ee script block important
                    if(env.BRANCH_NAME == 'main') {
                        bat "echo Deploying to PROD Server"
                    } else {
                        bat "echo Deploying to DEV Server"
                    }
                }
            }
        }
    }
}

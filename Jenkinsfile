pipeline {
    agent any
    tools {
        maven 'Maven3'  // Jenkins lo ee name undali
        jdk 'JDK17'
    } 
    trigger {
         cron ('H */4 * * *')
    }
    stages {
        stage('1. Build') {  // <-- ee stage add chey
            steps {
                bat "mvn clean package -DskipTests"
            }
        }
        stage('2. Deploy') {
            steps {
                echo "Deploying to ${env.BRANCH_NAME}"
                script { 
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

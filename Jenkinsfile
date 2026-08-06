pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK17'
    }

    triggers {
        pollSCM('H/5 *')  // every 5 minutes Git check chestundi
        // Leka
        // cron('H */4 * * *')  // every 4 hours build chestundi
    }

    stages {
        stage('1. Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('2. Deploy') {
            when {
                branch 'dev'
            }
            steps {
                bat 'echo Deploying to DEV Server'
            }
        }
        stage('3. Deploy') {
            when {
                branch 'main'
            }
            steps {
                bat 'echo Deploying to PROD Server'
            }
        }
    }
}

pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK17'
    }

    triggers {
        cron('H */4 * *')  // every 4 hours
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

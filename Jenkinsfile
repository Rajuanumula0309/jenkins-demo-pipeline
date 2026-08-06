pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK17'
    }

    triggers {
        pollSCM('H/5 *')
    }

    stages {
        stage('1. Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('2. Deploy to DEV') {
            when {
                branch 'dev'
            }
            steps {
                bat 'echo Deploying to DEV Server'
            }
        }
        stage('3. Deploy to PROD') {
            when {
                branch 'main'
            }
            steps {
                bat 'echo Deploying to PROD Server'
            }
        }
    }
}

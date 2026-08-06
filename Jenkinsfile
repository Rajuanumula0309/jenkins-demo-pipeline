pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK17'
    }

    triggers {
        cron('H */4 *')  // every 4 hours dev and main rendu auto build avutundi
    }

    stages {
        stage('1. Build') {
            steps {
                echo 'Starting Build...'
                bat 'mvn clean package'
            }
        }
        stage('2. Deploy to DEV') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying to DEV Server'
                bat 'echo Deployment to DEV Completed'
            }
        }
        stage('3. Deploy to PROD') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to PROD Server'
                bat 'echo Deployment to PROD Completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Finished Successfully ✅'
        }
        failure {
            echo 'Pipeline Failed ❌'
        }
    }
}

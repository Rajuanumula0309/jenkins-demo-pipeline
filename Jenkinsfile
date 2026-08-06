pipeline {
    agent any
    tools {
        maven 'Maven3'  // Maven name
        jdk 'JDK17'
    }
    stages {
        stage('2. Build with Maven') {
            steps {
                bat "mvn clean package -DskipTests"  // Rendu branches lo same build
            }
        }
        stage('4. Deploy') {
            steps {
                if(env.BRANCH_NAME == 'main') {
                    bat "echo Deploying to PROD Server"  // main lo idhi run avutundi
                } else {
                    bat "echo Deploying to DEV Server"   // dev lo idhi run avutundi
                }
            }
        }
    }
}

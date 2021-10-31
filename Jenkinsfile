pipeline{
    agent any
    stages{
        stage("Sonar Quality Check"){
            steps{
                echo "========executing Sonar Quality Check========"
                script {
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                    sh 'chmod +x gradlew'
                    sh './gradelw sonarqube'
                    }
                }
            }
        }
    }
}
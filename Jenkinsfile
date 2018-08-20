pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving files ...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
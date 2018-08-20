pipeline {
    agent any

    tools {
        maven 'localMaven'
    }
 
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean '
            }
            post {
                success {
                    echo 'Now Archiving ...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
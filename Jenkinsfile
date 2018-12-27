pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Limpando o pacote'
                bat 'mvn clean package'
            }
            post {
                success {
                    echo 'Arquivando'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
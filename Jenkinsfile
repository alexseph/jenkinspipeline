pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Limpando o pacote'
                sh 'mvn clean package'
            }
        }
        post {
            success {
                echo 'Arquivando'
                archiveArtifacts artifacts: '**/*.war'
            }
        }
    }
}
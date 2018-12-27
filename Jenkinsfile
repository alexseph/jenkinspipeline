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
            sucess {
                echo 'Arquivando'
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }
    }
}
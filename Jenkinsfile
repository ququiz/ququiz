pipeline {
    agent any
   
    stages {
        stage ('compose up') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/ququiz/ququiz']])
                sh 'docker compose up -d'
            }
        }
    }

}
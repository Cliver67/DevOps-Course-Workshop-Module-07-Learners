pipeline {
    
    agent {docker { image 'mcr.microsoft.com/dotnet/sdk:5.0' }}
    environment { 
        DOTNET_CLI_HOME = 'DOTNET_CLI_HOME'
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                echo 'Building..'
                sh "dotnet Build"

               
            }
        
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
pipeline {
    
    agent {docker { image 'mcr.microsoft.com/dotnet/sdk:5.0' }}
    environment { 
        DOTNET_CLI_HOME = '/tmp/dotnet_cli_home'
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                echo 'Building..'
                sh "dotnet build"

               
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
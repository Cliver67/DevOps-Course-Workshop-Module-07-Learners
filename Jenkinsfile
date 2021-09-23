pipeline {
    
    agent {docker { image 'mcr.microsoft.com/dotnet/sdk:5.0' }}
    
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
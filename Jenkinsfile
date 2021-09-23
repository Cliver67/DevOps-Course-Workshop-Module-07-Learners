pipeline {
    
    agent {docker { image 'mcr.microsoft.com/dotnet/sdk:5.0' }}
    environment { 
        DOTNET_CLI_HOME = '/tmp/dotnet_cli_home'
    }
    stages {
        stage('Build dotnet') {
            steps {
                checkout scm
                echo 'Building..'
                sh "dotnet build"
            }
        
        }
        stage('Test dot net') {
            steps {
                echo 'Testing..'
                sh "dotnet test"
            }
        }
        stage('Build Node') {
            agent {docker {image 'node:16-alpine'}}
            steps {
                echo 'Building Node....'
                dir("/DotnetTemplate.Web")
                sh "npm install"
                sh "npm run build"
                sh "npm t"
                sh "npm run lint"



            }
        }
    }
}
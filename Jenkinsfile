pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                run dotnet Build
               
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
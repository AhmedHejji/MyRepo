pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'dotnet restore pipeline.csproj'
                bat 'dotnet clean pipeline.csproj'
                bat 'dotnet build pipeline.csproj'
                archiveArtifacts artifacts: 'bin/**'
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

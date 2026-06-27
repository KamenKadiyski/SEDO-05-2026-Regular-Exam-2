pipeline {
    agent any
    stages {
        stage("Dotnet restore dependency") {
            when {
                branch 'main'
            }
            steps {
                sh "dotnet restore"
            }
        }
        stage("Dotnet build") {
            when {
                branch 'main'
            }
            steps {
                sh "dotnet build --no-restore"
            }
        }
        stage("Dotnet test") {
            when {
                branch 'main'
            }
            steps {
                sh "dotnet test --no-build --verbosity normal"
            }
        }
    }
}

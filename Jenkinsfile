pipeline {
    agent any
    stages {
        stage("Build and Test Application") {
            when {
                branch 'main'
            }
            stages {
                stage("Dotnet restore") {
                    steps {
                        sh "dotnet restore"
                    }
                }
                stage("Dotnet build") {
                    steps {
                        sh "dotnet build --no-restore"
                    }
                }
                stage("Dotnet test") {
                    steps {
                        sh "dotnet test --no-build --verbosity normal"
                    }
                }
            }
        }
    }
}

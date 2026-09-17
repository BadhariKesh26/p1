pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Select the deploy environment')
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'git remote add origin https://github.com/BadhariKesh26/p1.git']])
            }
        }
        stage('Show Parameter') {
            steps {
                echo "Selected environment: ${params.ENVIRONMENT}"
            }
        }
        stage('Build for Environment') {
            steps {
                echo "Building the application for the ${params.ENVIRONMENT} environment..."
            }
        }
    }
}
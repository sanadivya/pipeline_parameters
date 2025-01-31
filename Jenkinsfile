pipeline {
    agent any
    parameters {
        string( name: 'ENVIRONMENT', defaultValue: 'DEV', description: 'Set environment: DEV, TEST, or PROD')
    }
    stages{
        stage('Deploy to production'){
            when {
                expression { return params.ENVIRONMENT == 'PROD'}
            }
            steps {
                bat 'echo Deployed to production'
            }
        }
    }
}
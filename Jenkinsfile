// this is the jenkinsfile for the project

pipeline {
    // job will run on this agent
    // maching label 
    agent any
    parameters{
        choice(name: 'buildVersion', choices: ['1.0.0', '1.2.0', '1.3.0'], description: 'This will decide deployable build version of artifacts'),
        booleanParam(name: 'flagValue', defaultValue: false, description: 'Does test stage run?')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when{
                expression{
                    params.flagValue
                }
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying version : ${params.buildVersion}'
            }
        }
    }
}

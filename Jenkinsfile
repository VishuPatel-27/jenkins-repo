// this is the jenkinsfile for the project

pipeline {
    // job will run on this agent
    // maching label 
    agent { label 'ubuntu' || 'linux' }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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

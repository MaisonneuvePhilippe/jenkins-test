pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building... les filles et les garçons et les autres :) --'
                build job 'test1'
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

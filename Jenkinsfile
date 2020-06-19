pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build t he other pipeline'
                
                build job: 'pipe',
                parameters: [
                    string(name: 'MESSAGE', value: readFile(file: "./A")
                ]

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

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build t he other pipeline'
                @FILE = readFile("./A")
                build job: 'pipe',
                parameters: [
                    string(name: 'MESSAGE', value: @FILE)
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

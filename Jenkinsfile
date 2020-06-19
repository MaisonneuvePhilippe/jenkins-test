pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build t he other pipeline'
                build job: 'pipe',
                FILE = readFile("./A")
                parameters: [
                    string(name: 'MESSAGE', value: FILE)
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

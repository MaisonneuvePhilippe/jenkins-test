pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build t he other pipeline'
                def file = readFile("./A")
                build job: 'pipe',
                parameters: [
                    string(name: 'MESSAGE', value: file)
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

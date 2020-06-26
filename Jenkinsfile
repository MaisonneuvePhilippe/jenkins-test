pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build the other pipeline'
                
                build job: 'pipe',
                parameters: [
                    string(name: 'MESSAGE', value: readFile(file: "./A"))
                ]
                def workers_dir =  ".folder"
                def  FILES_LIST = sh (script: "ls   '${workers_dir}'", returnStdout: true).trim()

                echo "FILES_LIST : ${FILES_LIST}"
                //PARSING
                for(String ele : FILES_LIST.split("\\r?\\n")){ 
                println ">>>${ele}<<<"     
                }

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

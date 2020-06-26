pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Trying to build the other pipeline'
                
                // build job: 'pipe',
                // parameters: [
                //     string(name: 'MESSAGE', value: readFile(file: "./A"))
                // ]
                script{
                    def workers_dir =  "./folder"
                    def  FILES_LIST = sh (script: "ls   '${workers_dir}'", returnStdout: true).trim()
                    def full = ""
                    for (String elem: FILES_LIST.split("\\r?\\n")){
                        path = "./folder/"+elem
                        elem = "${elem}:${readFile(file: path)}"
                        full = full + elem + "|"
                        echo elem
                    }
                    //PARSING
                    echo full
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

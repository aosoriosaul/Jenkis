import groovy.json.JsonSlurperClassic

def jsonParse(def json){
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline{
    agent { label 'main'}
    environment { 
        appName = 'variable'
    }
    stages {
        stage("paso 1"){
            steps{
                script {
                    cmd "echo 'Hello World"
                }
            }
        }
    }
    post{
        always {
            deleteDirectory()
            cmd "echo 'fase always'"
        }
        success{
            cmd "echo 'face sucess"
        }
        failure{
            cmd "echo 'fase failure'"
        }
    }
}
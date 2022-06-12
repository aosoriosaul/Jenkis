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
                    sh "echo 'Hello World'"
                }
            }
        }
    }
    post{
        always {
            deleteDirectory()
                sh "echo 'fase always'"
        }
        success{
            sh "echo 'face sucess'"
        }
        failure{
            sh "eco 'fase failure'"
        }
    }
}

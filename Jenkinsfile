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
                    echo 'Hello World'
                }
            }
        }
    }
    post{
        always {
            deleteDirectory()
                echo 'fase always'
        }
        success{
            echo 'face sucess'
        }
        failure{
            echo 'fase failure'
        }
    }
}

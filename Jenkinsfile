import groovy.json.JsonSlurperClassic

def jsonParse(def json){
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline{
    agent any
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
            deleteDir()
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

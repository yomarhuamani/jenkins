import groovy.json.JsonSlurperClassic

def jsonParse(def json){
    new groovy.json.JsonSlurperClassic().parseText(json)
}

pipeline {
    agent { label= 'main' }
    environment {
        appName = 'dockerweb'
    }

    stages{
        stage("step one"){
            steps {
                script {
                    sh "echo 'Hello World'"
                 }
            }
        post{
            always{
                deleteDir()
                    sh "echo 'This will always run'"
            }
            success{
                sh "echo 'This will run only if successful'"
            }
            failure{
                sh "echo  'This will run only if failed'"
            }
        }
    }
 }
}
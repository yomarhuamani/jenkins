pipeline {
    agent any
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
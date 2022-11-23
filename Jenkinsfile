pipeline {
    agent any
    environment{
        ENV_URL= "pipeline.google.com"
    }

    stages {
        stage('first stage') {
            steps {
               sh 'echo one' 
               sh 'echo env_url is ${ENV_URL}'
            }
        }
        stage('second stage') {
            steps{
                echo 'two'
            }
        }
        stage('third stage'){
            steps{
                sh '''echo aws
                      echo devOps
                      echo ansible
                      echo jenkins'''
            }
        }
    }
}

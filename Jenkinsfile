pipeline {
    agent any
    environment{
        ENV_URL= "pipeline.google.com"
        AWS_ACCESS_KEY = credentials('AWS_ACCESS_KEY') 
    }

    stages {
        stage('first stage') {
            steps {
               sh 'echo one' 
               sh 'echo env_url is ${ENV_URL}'
               sh 'echo key is ${AWS_ACCESS_KEY}'
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

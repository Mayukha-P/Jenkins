pipeline {
    agent any
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment{
        ENV_URL= "pipeline.google.com"
        AWS_ACCESS_KEY = credentials('AWS_ACCESS_KEY') 
    }
    options{
        buildDiscarder(logRotator(numToKeepStr: '1'))
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

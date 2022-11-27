pipeline {
    agent { label 'java-node'}
    // parameters {
    //   string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    //    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    //}
   // triggers{ pollSCM('*/2 * * * *') }
    environment{
        ENV_URL= "pipeline.google.com"
        AWS_ACCESS_KEY = credentials('AWS_ACCESS_KEY') 
         SSH_CRED = credentials('SSH-CRED')
    }
    options{
         buildDiscarder(logRotator(numToKeepStr: '3'))
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'MINUTES')
    }
     tools {
            maven 'maven-3.5.0' 
        }

    stages {
        stage('parallet stage') {
        parallel {
        stage('first stage') {
            steps {
               sh "hostname"
               sh 'mvn --version'
               sh "echo One"
               sh "env"
               sh "sleep 10"
               sh 'echo one' 
              // sh 'echo env_url is ${ENV_URL}'
               //sh 'echo key is ${AWS_ACCESS_KEY}'
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
  }
}

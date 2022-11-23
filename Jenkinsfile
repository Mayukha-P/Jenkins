pipeline {
    agent any

    stages {
        stage('first stage') {
            steps {
                echo 'One'
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

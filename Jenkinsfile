//Declarative pipeline
pipeline {
    agent any 
    stages {
        stage("A"){
            script {
                sh'''
                    echo "We are in stage A"
                '''
            }
        }
        stage("B"){
            script {
                sh'''
                    echo "We are in stage B"
                '''
            }
        }
        stage("C"){
            script {
                sh'''
                    echo "We are in stage C"
                '''
            }
        }
    }
}
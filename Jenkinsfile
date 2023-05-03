//Declarative pipeline
pipeline {
    agent any 
    stages {
        stage("A"){
            steps {
                sh'''
                    echo "We are in stage A"
                    ls -l
                    mvn --version
                '''
            }
        }
        stage("B"){
            steps {
                sh'''
                    echo "We are in stage B"
                '''
            }
        }
        stage("C"){
            steps {
                sh'''
                    echo "We are in stage C"
                '''
            }
        }
    }
}
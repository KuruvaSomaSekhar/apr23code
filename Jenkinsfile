//Declarative pipeline
pipeline {
    agent any 
     parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'master', description: 'provide branch name')
    }   
    stages {
        stage("Build"){
            steps {
                sh'''
                    echo "We are in stage A"
                    ls -l
                    mvn --version
                    mvn clean package
                '''
            }
        }
        stage("Upload artifacts"){
            steps {
                sh'''
                    echo "We are in stage B"
                    ls -l target/
                    echo $JOB_NAME
                    echo ${BRANCH_NAME}
                    echo ${params.BRANCH_NAME}
                    echo $BUILD_NUMBER
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
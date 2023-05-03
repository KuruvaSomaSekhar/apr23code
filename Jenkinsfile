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
                    echo $BUILD_NUMBER
                    aws s3 cp target/devops-1.0.0.war s3://apr23artifacts/$JOB_NAME/${BRANCH_NAME}/$BUILD_NUMBER/
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
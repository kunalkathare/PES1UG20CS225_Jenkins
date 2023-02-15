pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myprog new.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './myprog'
                sh 'build PES1UG20CS225-1'
                echo 'Test Stage Successful'
                post {
                    always {
                        junit 'target/surefire-reports/*.xml'
                    }
                }
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

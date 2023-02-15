pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myprog new.cpp'
                sh 'build 'PES1UG20CS225-1''
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './myprog'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Stage Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

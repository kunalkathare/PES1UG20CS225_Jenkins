pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myprog new.cpp'
                sh 'build 'curl -I -u admin:admin http://localhost:8080/job/PES1UG20CS225-1/build\?token\=1100c4a3a1d30486169e06dedb17b09d49'
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

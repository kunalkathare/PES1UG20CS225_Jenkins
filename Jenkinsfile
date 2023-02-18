pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o new new.cpp'
                build job: 'PES1UG20CS225-1'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './neww'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy Stage Successful'
                sh 'cat Keerthana.txt' -> use for showing error
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

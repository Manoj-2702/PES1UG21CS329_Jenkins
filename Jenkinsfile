pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS331-1'
                sh 'g++ main/hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
                sh 'exit 1' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
   
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

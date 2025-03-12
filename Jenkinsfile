pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS904_1'
                sh 'g++ main.cpp -o output'  // Correct file name
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

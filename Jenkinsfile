pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS904_1'
                sh 'g++ wrongfile.cpp -o output'  // Intentional error (wrong file name)
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh 'chmod +x main/hello_exec && ./main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment successful!"
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

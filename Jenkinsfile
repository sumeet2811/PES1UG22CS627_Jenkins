pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    g++ main/hello.cpp -o main/hello_exec
                    '''
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh '''
                    ./main/hello_exec
                    '''
                }
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

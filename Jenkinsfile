pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the C++ code
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // Execute the compiled program
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                // Deployment steps go here
                echo 'Deployment completed'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

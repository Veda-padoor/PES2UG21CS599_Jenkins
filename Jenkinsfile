pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output main.cpp' // Compile the C++ code
            }
        }
        stage('Test') {
            steps {
                sh './output' // Execute the compiled program
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...' // Placeholder for deployment steps
                // You can add deployment commands here, such as copying files to a server
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

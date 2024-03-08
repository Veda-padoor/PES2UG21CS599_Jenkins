pipeline {
    agent any
    stage('Clone repository) {
        steps {
            checkout ([$class: "GitSCM',
            branches: [[name: '*/main']],
            userRemoteConfigs: [[url: 'https://github.com/Veda-padoor/PES2UG21CS599_Jenkins.git']]])
        }
    }
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS599-1'
                sh 'g++ main.cpp -o output'
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
post{
    failure{
        error 'Pipeline failed'
    }
}
}
